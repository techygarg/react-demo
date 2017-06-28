node {
    checkout scm
    docker.image('node:6.11.0').inside {
        stage('Build') {

            sh 'npm --version'
            sh 'npm install'
            sh 'npm run build'
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'npm test'
            }
        }
        stage('Deploy') {
        steps {
            echo 'Deploying....'
            }
        }
    }
}

