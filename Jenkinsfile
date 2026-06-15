pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
                RUN echo "ARYAN DEBUG"
RUN npm list next
            }
        }

        stage('Build') {
            steps {
                bat 'docker compose build --no-cache'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker compose down'
                bat 'docker compose up -d'
            }
        }

        stage('Verify') {
            steps {
                bat 'docker ps'
            }
        }
    }
}
