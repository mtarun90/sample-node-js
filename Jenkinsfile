node {
    // Define the Docker image
    def nodeImage = '394abc79672f'

    // Run the pipeline inside the Docker container
    docker.image(the-example-app.nodejs).inside {
        stage('Build') {
            echo 'Installing dependencies...'
            sh 'npm install'
        }

        stage('Deploy') {
            echo 'Starting application...'
            sh 'npm run start:dev'
        }
    }
}
