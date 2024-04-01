pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/NaseemKhan005/react-bank-app.git'
            }
        }
        
        stage('Dependency Installation') {
            steps {
                // Add commands to install backend dependencies here
                // For example:
                sh 'npm install'
            }
        }
        
        stage('Test') {
            steps {
                // Add commands to run tests for the backend
                // For example:
                sh 'npm test'
            }
        }
    }
}
