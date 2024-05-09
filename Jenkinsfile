pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Build Status: ${currentBuild.result}",
                        body: "Build completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests using JUnit'
                echo 'Running integration tests'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Unit and Integration Tests Status: ${currentBuild.result}",
                        body: "Unit and Integration Tests completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                echo 'Running code analysis'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Code Analysis Status: ${currentBuild.result}",
                        body: "Code Analysis completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Performing security scan'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Security Scan Status: ${currentBuild.result}",
                        body: "Security Scan completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying application to staging server'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Deploy to Staging Status: ${currentBuild.result}",
                        body: "Deployment to Staging completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Integration Tests on Staging Status: ${currentBuild.result}",
                        body: "Integration Tests on Staging completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo 'Deploying application to production server'
            }
            post {
                always {
                    emailext (
                        to: 'gpranav2901@gmail.com',
                        subject: "Deploy to Production Status: ${currentBuild.result}",
                        body: "Deployment to Production completed with status: ${currentBuild.result}."
                    )
                }
            }
        }
    }
}
