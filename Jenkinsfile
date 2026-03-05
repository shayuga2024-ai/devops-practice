pipeline {
    agent any

    environment {
        IMAGE_NAME = "shayuga/devops-app"
    }

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %IMAGE_NAME% .'
            }
        }

        stage('Push to DockerHub') {
            steps {
                bat 'docker push %IMAGE_NAME%'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8082:80 %IMAGE_NAME%'
            }
        }

    }
}
