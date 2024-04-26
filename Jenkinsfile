pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "/Users/vv/Desktop/Professional practice/Task 5.1P"
        TESTING_ENVIRONMENT = "TestEnv"
        PRODUCTION_ENVIRONMENT = "Sri Varshini"
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Fetching source code from ${env.DIRECTORY_PATH}"
                echo "Compiling the code and generating artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Running unit tests"
                echo "Running integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application to ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                script {
                    echo "Waiting for manual approval..."
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying to production environment (${env.PRODUCTION_ENVIRONMENT})"
            }
        }
    }
}
