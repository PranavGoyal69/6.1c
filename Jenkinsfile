pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests using JUnit'
                echo 'Running integration tests'
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis'
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing security scan'
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying application to staging server'
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying application to production server'
            }
        }
    }
    
    post {
        success {
            // Send notification email upon successful completion
            emailext (
                to: 'gpranav2901@gmail.com',
                subject: "Pipeline Status: SUCCESS",
                body: "Pipeline completed successfully.",
                attachmentsPattern: '**/*.log'
            )
        }
        failure {
            // Send notification email upon failure
            emailext (
                to: 'gpranav2901@gmail.com',
                subject: "Pipeline Status: FAILURE",
                body: "Pipeline failed. Please check logs for details.",
                attachmentsPattern: '**/*.log'
            )
        }
    }
}
