pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Pulling code from GitHub....."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                // Example build command
                sh 'echo "Build step running"'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example test command
                sh 'echo "Tests executed"'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                // Example deploy command
                sh 'echo "Deploy step running"'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
