pipeline {
    agent {
        docker {
            image 'node:14'
        }
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Installing dependencies...'
                    sh 'npm install'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Starting application...'
                    sh 'npm run start:dev'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Notify or take corrective actions here.'
        }
    }
}
