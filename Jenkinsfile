pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
            
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                // Add your build steps here
                echo 'Performing build...'
            }
        }
        
      
        
        stage('Deploy') {
            steps {
                // Add your deployment steps here
                echo 'Deploying...'
            }
        }
    }
    
    post {
        success {
            // Actions to be performed on successful execution
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to be performed on failure
            echo 'Pipeline failed!'
        }
    }
}


