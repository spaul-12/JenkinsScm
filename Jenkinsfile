pipeline {
    agent any

    environment {
        DIRECTORY_PATH     = '/home/jenkins/workspace/myapp'
        TESTING_ENVIRONMENT  = 'staging-env'
        PRODUCTION_ENVIRONMENT = 'Subhrajit Paul'  
    }

    stages {
        stage('Build') {
            steps {
                echo 'Stage 1 Build: Compiling and packaging code using Maven. build No. 4'
                echo 'Tool: Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2 Unit and Integration Tests: Running unit tests and integration tests.'
                echo 'Tools: JUnit (unit tests), TestNG (integration tests)'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Stage 3 Code Analysis: Analysing code quality against industry standards.'
                echo 'Tool: SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Stage 4 Security Scan: Scanning code for known vulnerabilities.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5 Deploy: Deploying application to staging environment.'
                echo 'Tool: AWS CLI / AWS EC2'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6 Integration Tests: Running integration tests in staging environment.'
                echo 'Tool: Selenium'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Stage 7 Deploy to Production: Deploying application to production environment.'
                echo 'Tool: AWS CLI / AWS EC2'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Please check the logs."
        }
    }
}