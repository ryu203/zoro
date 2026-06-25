pipeline {
    agent any

    stages {
        stage('clone Repository') {
            git branch: 'main',
                url:'https://github.com/ryu203/zoro.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker builder -t DockerDemo .'
            }
        }
        stage('Run Docker container') {
            steps {
                bat 'docker run -d -p 8080:80 DockerDemo'
            }
        }
    }
}