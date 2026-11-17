pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { checkout scm }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t student-form .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker rm -f student-form-container 2>NUL'
                bat 'docker run -d -p 8080:80 --name student-form-container student-form'
            }
        }
    }
}
