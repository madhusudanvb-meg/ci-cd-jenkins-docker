pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/madhusudanvb-meg/ci-cd-jenkins-docker.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-cicd-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 my-cicd-app'
            }
        }
    }
}
