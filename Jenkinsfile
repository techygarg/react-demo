pipeline {
 agent { docker 'node:6.11.0' }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
}