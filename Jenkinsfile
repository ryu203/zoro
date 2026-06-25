pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ryu203/zoro.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t dockerdemo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8080:80 --name dockerdemocontainer dockerdemo'
            }
        }

    }
}