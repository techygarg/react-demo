#!groovy


node('node') {


    currentBuild.result = "SUCCESS"

    try {

       stage('Checkout'){

          checkout scm
       }

       stage('Test'){

         sh 'npm install'
         sh 'npm test'

       }

       stage('Build Docker'){

            sh 'npm run build'
       }

       stage('Deploy'){

         echo 'Push to Repo'
         echo 'ssh to web server and tell it to pull new image'
       }

       stage('Cleanup'){

         echo 'prune and cleanup'
         sh 'npm prune'
         sh 'rm node_modules -rf'
       }



    }
    catch (err) {

        currentBuild.result = "FAILURE"

            mail body: "project build error is here: ${env.BUILD_URL}" ,
            from: 'xxxx@yyyy.com',
            replyTo: 'yyyy@yyyy.com',
            subject: 'project build failed',
            to: 'zzzz@yyyyy.com'

        throw err
    }

}
