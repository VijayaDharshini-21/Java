pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'javac Calculator.java'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add commands to run tests here (if applicable)
                // For example: sh 'java CalculatorTest'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // Add commands to deploy the project here (if applicable)
                // For example: sh 'scp Calculator.jar user@server:/path/to/deploy'
            }
        }
    }
}
