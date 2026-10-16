
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code is available in the workspace'
                bat 'dir'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project'
                bat 'echo Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project'
                bat 'if exist README.md (echo README found) else (exit /b 1)'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline completed successfully!'
        }
        failure {
            echo 'CI pipeline failed. Check the console output.'
        }
    }
}
