pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Build Status: SUCCESS",
                    body: "Build completed successfully."
                )
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests using JUnit'
                echo 'Running integration tests'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Unit and Integration Tests Status: SUCCESS",
                    body: "Unit and Integration Tests completed successfully."
                )
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Code Analysis Status: SUCCESS",
                    body: "Code Analysis completed successfully."
                )
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing security scan'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Security Scan Status: SUCCESS",
                    body: "Security Scan completed successfully."
                )
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying application to staging server'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Deploy to Staging Status: SUCCESS",
                    body: "Deployment to Staging completed successfully."
                )
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Integration Tests on Staging Status: SUCCESS",
                    body: "Integration Tests on Staging completed successfully."
                )
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying application to production server'
                // Add email notification after the stage
                emailext (
                    to: 'gpranav2901@gmail.com',
                    subject: "Deploy to Production Status: SUCCESS",
                    body: "Deployment to Production completed successfully."
                )
            }
        }
    }
}
