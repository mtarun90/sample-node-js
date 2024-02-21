pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from GitHub
                git 'https://github.com/mtarun90/sample-node-js.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install Node.js dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                
                    sh 'npm run build'
                }
            }
        }

