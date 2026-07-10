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
                sh 'python3 -m pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Testing...'
                sh 'python3 -m pytest'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python3 app.py'
            }
        }
        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying the application...'
        //     }
        // }
    }
}
