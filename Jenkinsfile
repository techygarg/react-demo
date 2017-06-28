node {
    checkout scm
    docker.image('node:6.3').inside {
        stage('Build') {

            sh 'npm --version'
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

