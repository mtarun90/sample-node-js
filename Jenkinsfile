node {
    // Define the Docker image
    def nodeImage = 'node:latest'

    // Run the pipeline inside the Docker container
    docker.image(394abc79672f).inside {
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
