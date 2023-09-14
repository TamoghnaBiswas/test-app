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
                    sh 'docker build -t tbiswas007/pythonapp:0.0.1 .'

                    // Log in to Docker Hub
                    sh 'docker login -u tbiswas007 -p Tamoghna@b1'

                    // Push the Docker image to Docker Hub
                    sh 'docker push tbiswas007/pythonapp:0.0.1'
                }
            }
        }
    }
}
