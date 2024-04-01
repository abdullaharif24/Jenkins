pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Dependency Installation') {
            steps {
                // Install dependencies for backend
                bat 'npm install'
            }
        }
        
        stage('Test') {
            steps {
                // Placeholder step for running tests
                echo 'Running tests...'
            }
        }
        
        stage('Containerized') {
            steps {
                // Build and deploy containers using Docker Compose
                bat 'docker-compose up -d --build'
            }
            post {
                always {
                    // Cleanup - stop and remove containers
                    bat 'docker-compose down'
                }
            }
        }
    }
}
