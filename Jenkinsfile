pipeline {
    agent any

    stages {
        stage('Build and Run Docker Container') {
            steps {
                script {
                    // Pull or build your Docker image
                    docker.image('mtarun90/tarunrep:latest').pull()

                    // Run the Docker container
                    def dockerContainer = docker.image('mtarun90/tarunrep:latest').run('-p 8080:80')

                    // Execute commands inside the running container
                    dockerContainer.inside {
                        sh 'echo "Commands to run inside the Docker container"'
                        sh 'ls -la'
                        // Add any other commands you need
                    }
                }
            }
        }
    }

    post {
        success {
            // Notify or perform actions on successful build
            echo 'Pipeline succeeded. Notify or perform actions here.'
        }
        failure {
            // Notify or perform actions on failed build
            echo 'Pipeline failed. Notify or perform actions here.'
        }
    }
}
