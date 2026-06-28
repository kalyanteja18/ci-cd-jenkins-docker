pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t flask-app .'
            }
        }

        stage('Run App') {
            steps {
                echo 'Running the app...'
                sh 'docker stop flask-app-container || true'
                sh 'docker rm flask-app-container || true'
                sh 'docker run -d --name flask-app-container -p 5000:5000 flask-app'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
