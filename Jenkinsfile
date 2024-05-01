pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build the code using Maven
                echo "Building the code using Maven and then integrating"
            }
        }       
        stage('Unit and Integration Tests') {
            steps {
                
                // Run unit tests using JUnit
                echo "Running unit tests using j unit sds"
                // Run integration tests using Selenium
                echo "Running integration tests using Selenium"
            }
            post {
        always {
            // Send email with build log file as attachment
            emailext (
                to: 'faritzafar0@gmail.com',
                subject: "Pipeline ${currentBuild.result}: ${env.JOB_NAME} ${env.BUILD_NUMBER}",
                body: "The pipeline has completed with result ${currentBuild.result}.",
                attachmentsPattern: 'logs/*.log',
                attachLog: true
            )
        }
        }
        
        stage('Code Analysis') {
            steps {
                // Integrate a code analysis tool (e.g., SonarQube)
                echo "Integrating code analysis tool (e.g., SonarQube)"
            }
        }
        stage('Security Scan') {
            steps {
                // Perform a security scan using OWASP ZAP
                echo "Performing security scan using OWASP ZAP"
            }
            post {
        always {
            // Send email with build log file as attachment
            emailext (
                to: 'faritzafar0@gmail.com',
                subject: "Pipeline ${currentBuild.result}: ${env.JOB_NAME} ${env.BUILD_NUMBER}",
                body: "The pipeline has completed with result ${currentBuild.result}.",
                attachmentsPattern: 'logs/*.log',
                attachLog: true
            )
        }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy the application to a staging server (e.g., AWS EC2 instance)
                echo "Deploying the application to staging server (e.g., AWS EC2 instance)"
            }
        }
        stage('Integration Tests on Staging') {
            
            steps {
                // Run integration tests on the staging environment
                echo "Running integration tests on staging environment"
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy the application to a production server (e.g., AWS EC2 instance)
                echo "Deploying the application to production server (e.g., AWS EC2 instance)"
            }
        }
    }
    
    post {
        always {
            // Send email with build log file as attachment
            emailext (
                to: 'faritzafar0@gmail.com',
                subject: "Pipeline ${currentBuild.result}: ${env.JOB_NAME} ${env.BUILD_NUMBER}",
                body: "The pipeline has completed with result ${currentBuild.result}.",
                attachmentsPattern: 'logs/*.log',
                attachLog: true
            )
        }
    }
}


