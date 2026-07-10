pipeline {
    agent any

    stages {
        stage('Checkout code') {
            steps {
                echo 'Checking out code from github...'
                checkout scm
            }
        }
        stage('Install dependencies') {
            steps {
                echo 'Installing dependencies'
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Testing...'
                sh 'pytest test_app.py'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python app.py'
            }
        }
        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying the application...'
        //     }
        // }
    }
}