pipeline {
    agent any

    parameters {
        string(name: 'USERNAME', defaultValue: 'sriram', description: 'Enter username')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run test stage?')
        choice(name: 'ENV', choices: ['dev', 'qa', 'prod'], description: 'Select environment')
    }

    stages {

        stage('Print Params') {
            steps {
                echo "Username: ${params.USERNAME}"
                echo "Run Tests: ${params.RUN_TESTS}"
                echo "Selected ENV: ${params.ENV}"
            }
        }

        stage('Build') {
            steps {
                echo "Building application for environment: ${params.ENV}"
            }
        }

        stage('Test') {
            when {
                expression { params.RUN_TESTS == true }
            }
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to ${params.ENV} environment..."
            }
        }
    }
}