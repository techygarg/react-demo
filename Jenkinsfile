node('docker') {
    checkout scm
    stage('Build') {
         docker.image('node:6.3').inside {
        sh 'npm --version'
    }
    }
    stage('Test') {
        steps {
            echo 'Testing..'
        }
    }
    stage('Deploy') {
    steps {
        echo 'Deploying....'
        }
    }
}

