pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from version control (GitHub, GitLab, etc.)
                checkout scm
            }
        }
        
        stage('Build Docker Image') {
            steps {
                // Run Docker build command in the shell
                sh 'docker build -t my-nginx-image:latest .'
            }
        }

        stage('Run Docker Container') {
            steps {
                // Run Docker container in the shell
                sh 'docker run -d -p 8080:80 my-nginx-image:latest'
            }
        }
    }
}
