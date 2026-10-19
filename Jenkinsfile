
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t adrios12-app:latest .'
            }
        }

        stage('Test Website') {
            steps {
                bat 'docker image inspect adrios12-app:latest'
                echo 'Docker image built successfully!'
            }
        }
    }
}
