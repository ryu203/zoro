pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t dockerdemo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker rm -f dockerdemocontainer || exit 0'
                bat 'docker run -d -p 8081:80 --name dockerdemocontainer dockerdemo'
            }
        }

    }
}