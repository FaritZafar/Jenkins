pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Build the code using Maven
                    sh 'mvn clean package'
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                script {
                    // Run unit tests
                    sh 'mvn test'
                    // Run integration tests (e.g., with Selenium)
                    sh 'mvn verify'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrate SonarQube for code analysis
                // Execute SonarQube scanner
            }
        }
        stage('Security Scan') {
            steps {
                // Integrate OWASP ZAP for security scan
                // Execute ZAP security scan
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy the application to AWS EC2 instance
                // Use Jenkins deployment plugin or AWS CLI
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on the staging environment
                // Use Selenium or similar tools
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy the application to production server (AWS EC2)
            }
        }
    }
}
