pipeline {
    agent any

    stages {
        stage('install pm2') {
            steps {
                sh 'sudo npm install -g pm2'
            }
        }

        stage('build') {
            steps {
                sh sudo 'npm install'
           
                }
            }
        

        stage('deploy') {
            steps {
                
                    sh 'sudo pm2 start bin/www'
                }
            }
        }
}

