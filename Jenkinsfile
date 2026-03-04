pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/shayuga2024-ai/devops-practice.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8081:80 devops-app'
            }
        }

    }
}
