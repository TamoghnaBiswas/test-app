pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from the repository
                checkout scm
            }
        }

        stage('Build and Push Docker Image') {
            steps {
                script {
                    // Build a Docker image from your Python app
                    sh 'docker build -t your-docker-username/your-app-name:latest .'

                    // Log in to Docker Hub
                    sh 'docker login -u your-docker-username -p your-docker-password'

                    // Push the Docker image to Docker Hub
                    sh 'docker push your-docker-username/your-app-name:latest'
                }
            }
        }
    }
}
