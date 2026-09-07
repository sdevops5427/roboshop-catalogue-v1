pipeline {

    agent any

    stages {
        stage('CheckOut') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sdevops5427/roboshop-catalogue-v1.git'
            }
        }
        stage('Build Image') {
            steps {
                sh "docker build -t catalogue ."
            }
        }
        stage('Tag Image') {
            steps {
                sh "docker tag catalogue roboshop0088.azurecr.io/catalogue:latest"
            }
        }
        stage('Push Image') {
            steps {
                sh "docker push roboshop0088.azurecr.io/catalogue"
            }
        }
    }
}
