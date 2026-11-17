pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Fetching source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application'
                sh 'mkdir -p build'
                sh 'cp index.html build/'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application'
                sh 'test -f build/index.html'
                echo 'Test passed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
                echo 'Application deployed successfully'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}
