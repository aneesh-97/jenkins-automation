pipeline {
    agent { label 'windows' }

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t seqato/demo-app .'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                bat 'docker push seqato/demo-app:latest'
            }
        }
    }
}
