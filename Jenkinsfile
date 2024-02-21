pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/mtarun90/sample-node-js.git/'
            }
        }

        stage('Build and Run Container') {
            steps {
                script {
                    // Build Docker image
                    sh 'docker build -t the-example-app.nodejs .'

                    // Run Docker container
                    sh 'docker run -p 3000:3000 -d the-example-app.nodejs'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the logs for details.'
        }
    }
}
