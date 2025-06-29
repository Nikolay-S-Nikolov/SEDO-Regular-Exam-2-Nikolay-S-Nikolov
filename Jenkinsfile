pipeline {
    agent any

    stages {
        stage('Checkout the code') {
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps {
                checkout scm
            }
        }

        stage('Build the project') {
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps {
                checkout scm
                echo 'Building the application...'
                bat 'dotnet build'
            }
        }

        stage('Run all tests') {
            when {
                anyOf {
                    branch 'main'
                }
            }
            steps {
                echo 'Running tests...'
                bat 'dotnet test'
            }
        }
    }
}