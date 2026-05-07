pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t myapp .'
            }
        }

        stage('Verify Docker') {
            steps {
                bat 'docker images'
            }
        }

    }
}