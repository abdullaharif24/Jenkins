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
                // Install dependencies for frontend
                bat 'npm install'
                // Install dependencies for backend (if any)
                // sh 'command_to_install_backend_dependencies'
            }
        }
        
        stage('Build') {
            steps {
                // Build React application
                bat 'npm start'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests for React application
                bat 'npm test'
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