pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from GitHub
                git 'https://github.com/mtarun90/sample-node-js.git'
            }
        }

        stage('Build and Run Docker Container') {
            steps {
                script {
                    // Build Docker image
                    def dockerImage = docker.build('136ca99b4b96:latest', './the-example-app.nodejs')

                    // Run Docker container
                    dockerImage.run('-p 8080:80 -d')
                }
            }
        }

        stage('Deploy') {
            steps {
                // Your deployment steps go here
            }
        }
    }

    post {
        always {
            // Cleanup steps go here, e.g., stop and remove the container
            script {
                sh 'docker stop your-container-name || true'
                sh 'docker rm your-container-name || true'
            }
        }
    }
}
