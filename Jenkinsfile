pipeline {
    agent any

    stages {
        stage('Checkout the code') {
            steps {
                checkout scm
            }
        }

        stage('Build the project') {
            steps {
                echo 'Building the application...'
                bat 'dotnet build'
            }
        }

        stage('Run all tests') {
            steps {
                echo 'Running tests...'
                bat 'dotnet test'
            }
        }
    }
}
