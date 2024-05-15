pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from Git
                git 'https://github.com/sawhenayhtoo/Invoice.git'
            }
        }
        
        stage('Build') {
            steps {
                // Example build steps, replace with your actual build commands
                sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                // Example test steps, replace with your actual test commands
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Example deployment steps, replace with your actual deployment commands
                sh 'mvn deploy'
            }
        }
    }
    
    post {
        success {
            // Actions to take if the pipeline succeeds
            echo 'Pipeline succeeded! Deploying...'
            // Add deployment steps here
        }
        
        failure {
            // Actions to take if the pipeline fails
            echo 'Pipeline failed! Sending notification...'
            // Add notification steps here
        }
        
        always {
            // Actions to take regardless of pipeline outcome
            echo 'Cleaning up workspace...'
            // Add cleanup steps here
        }
    }
}
