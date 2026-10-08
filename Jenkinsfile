pipeline {
    agent any

    environment {
        DOCKER = 'C:\\Users\\Newt\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe'
    }

    stages {
        stage('Build') {
            steps {
                bat '"%DOCKER%" build -t task-2-app .'
            }
        }

        stage('Test') {
            steps {
                bat '"%DOCKER%" images task-2-app'
            }
        }

        stage('Deploy') {
            steps {
                bat '"%DOCKER%" stop task-2-container || exit /b 0'
                bat '"%DOCKER%" rm task-2-container || exit /b 0'
                bat '"%DOCKER%" run -d -p 8081:80 --name task-2-container task-2-app'
            }
        }
    }
}