pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'docker build -t task-2-app .'
            }
        }

        stage('Test') {
            steps {
                bat 'docker images task-2-app'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker stop task-2-container || exit 0'
                bat 'docker rm task-2-container || exit 0'
                bat 'docker run -d -p 8081:80 --name task-2-container task-2-app'
            }
        }
    }
}