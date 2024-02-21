pipeline {
    agent any
    stages{
       // stage('Install PM2'){
       //     steps{
       //         sh 'npm install -g pm2'
       //    }
       // }
        stage('Build'){
            steps{
                sh 'npm install'
            }
        }
        stage('Deploy'){
            steps{
                sh 'npm run start:dev'
    }
    }
    }
}
