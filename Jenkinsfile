pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Build code using Maven (or any build tool)
                    sh 'mvn clean package' // Example Maven command
                }
            }
        }
        stage('Unit & Integration Tests') {
            steps {
                script {
                    // Run unit tests with JUnit (or any testing framework)
                    sh 'mvn test' // Example Maven command for JUnit tests
                    // Run integration tests with a tool like Selenium
                    sh './integration_tests.sh' // Example script for integration tests
                }
                post {
                    success {
                        // Send notification email on success with test logs attached
                        emailext body: 'Unit & Integration Tests Successful!', 
                            subject: 'Pipeline - Unit & Integration Tests (Success)', 
                            recipientEmails: 'gpranav2901@gmail.com', 
                            attachLog: true
                    }
                    failure {
                        // Send notification email on failure with test logs attached
                        emailext body: 'Unit & Integration Tests Failed!', 
                            subject: 'Pipeline - Unit & Integration Tests (Failure)', 
                            recipientEmails: 'gpranav2901@gmail.com', 
                            attachLog: true
                    }
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    // Analyze code with SonarQube (or similar tool)
                    sh 'sonar-scanner -DprojectKey=your_project_key ...' // Example SonarQube scanner command
                }
            }
            post {
                always {
                    // Send notification email with code analysis report (if applicable)
                    emailext body: 'Code Analysis Report Attached!', 
                        subject: 'Pipeline - Code Analysis Report', 
                        recipientEmails: 'gpranav2901@gmail.com', 
                        attachLog: true // Modify if report attachment is supported
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    // Scanning for vulnerabilities with SAST tool like Snyk
                    sh 'snyk test ...' // Example Snyk command
                }
            }
            post {
                success {
                    // Send notification email on success with security scan report (if applicable)
                    emailext body: 'Security Scan Successful!', 
                        subject: 'Pipeline - Security Scan (Success)', 
                        recipientEmails: 'gpranav2901@gmail.com', 
                        attachLog: true // Modify if report attachment is supported
                }
                failure {
                    // Send notification email on failure with security scan report (if applicable)
                    emailext body: 'Security Scan Failed!', 
                        subject: 'Pipeline - Security Scan (Failure)', 
                        recipientEmails: 'gpranav2901@gmail.com', 
                        attachLog: true // Modify if report attachment is supported
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    // Deploying application to a staging server (e.g., AWS EC2)
                    // Replace with your deployment script (e.g., using AWS CLI)
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    // Running integration tests on the staging environment
                    // Replace with your script for testing on the staging server
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    // Deploying application to production server (e.g., AWS EC2)
                    // Replace with your script (e.g., using AWS CLI)
                }
            }
        }
    }
}
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Build code using Maven (or any build tool)
                    sh 'mvn clean package' // Example Maven command
                }
            }
        }
        stage('Unit & Integration Tests') {
            steps {
                script {
                    // Run unit tests with JUnit (or any testing framework)
                    sh 'mvn test' // Example Maven command for JUnit tests
                    // Run integration tests with a tool like Selenium
                    sh './integration_tests.sh' // Example script for integration tests
                }
                post {
                    success {
                        // Send notification email on success with test logs attached
                        emailext body: 'Unit & Integration Tests Successful!', 
                            subject: 'Pipeline - Unit & Integration Tests (Success)', 
                            recipientEmails: 'gpranav2901@gmail.com', 
                            attachLog: true
                    }
                    failure {
                        // Send notification email on failure with test logs attached
                        emailext body: 'Unit & Integration Tests Failed!', 
                            subject: 'Pipeline - Unit & Integration Tests (Failure)', 
                            recipientEmails: 'gpranav2901@gmail.com', 
                            attachLog: true
                    }
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    // Analyze code with SonarQube (or similar tool)
                    sh 'sonar-scanner -DprojectKey=your_project_key ...' // Example SonarQube scanner command
                }
            }
            post {
                always {
                    // Send notification email with code analysis report (if applicable)
                    emailext body: 'Code Analysis Report Attached!', 
                        subject: 'Pipeline - Code Analysis Report', 
                        recipientEmails: 'gpranav2901@gmail.com', 
                        attachLog: true // Modify if report attachment is supported
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    // Scanning for vulnerabilities with SAST tool like Snyk
                    sh 'snyk test ...' // Example Snyk command
                }
            }
            post {
                success {
                    // Send notification email on success with security scan report (if applicable)
                    emailext body: 'Security Scan Successful!', 
                        subject: 'Pipeline - Security Scan (Success)', 
                        recipientEmails: 'gpranav2901@gmail.com', 
                        attachLog: true // Modify if report attachment is supported
                }
                failure {
                    // Send notification email on failure with security scan report (if applicable)
                    emailext body: 'Security Scan Failed!', 
                        subject: 'Pipeline - Security Scan (Failure)', 
                        recipientEmails: 'gpranav2901@gmail.com', 
                        attachLog: true // Modify if report attachment is supported
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    // Deploying application to a staging server (e.g., AWS EC2)
                    // Replace with your deployment script (e.g., using AWS CLI)
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    // Running integration tests on the staging environment
                    // Replace with your script for testing on the staging server
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    // Deploying application to production server (e.g., AWS EC2)
                    // Replace with your script (e.g., using AWS CLI)
                }
            }
        }
    }
}
