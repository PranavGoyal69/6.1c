pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the code using Maven'
                    // Build code using Maven (or any build tool)
                    sh 'mvn clean package' // Example Maven command
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Build Status: ${currentBuild.result}",
                            body: "Build completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Running unit tests using JUnit'
                    echo 'Running integration tests'
                    // Run unit tests with JUnit (or any testing framework)
                    sh 'mvn test' // Example Maven command for JUnit tests
                    // Run integration tests with a tool like Selenium
                    sh './integration_tests.sh' // Example script for integration tests
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Unit and Integration Tests Status: ${currentBuild.result}",
                            body: "Unit and Integration Tests completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Running code analysis'
                    // Analyze code with SonarQube (or similar tool)
                    sh 'sonar-scanner -DprojectKey=your_project_key ...' // Example SonarQube scanner command
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Code Analysis Status: ${currentBuild.result}",
                            body: "Code Analysis completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                script {
                    echo 'Performing security scan'
                    // Scanning for vulnerabilities with SAST tool like Snyk
                    sh 'snyk test ...' // Example Snyk command
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Security Scan Status: ${currentBuild.result}",
                            body: "Security Scan completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying application to staging server'
                    // Deploying application to a staging server (e.g., AWS EC2)
                    // Replace with your deployment script (e.g., using AWS CLI)
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Deploy to Staging Status: ${currentBuild.result}",
                            body: "Deployment to Staging completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running integration tests on staging environment'
                    // Running integration tests on the staging environment
                    // Replace with your script for testing on the staging server
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Integration Tests on Staging Status: ${currentBuild.result}",
                            body: "Integration Tests on Staging completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying application to production server'
                    // Deploying application to production server (e.g., AWS EC2)
                    // Replace with your script (e.g., using AWS CLI)
                }
                post {
                    always {
                        // Send notification email after the stage
                        emailext (
                            to: 'gpranav2901@gmail.com',
                            subject: "Deploy to Production Status: ${currentBuild.result}",
                            body: "Deployment to Production completed with status: ${currentBuild.result}.",
                            attachLog: true
                        )
                    }
                }
            }
        }
    }
}
