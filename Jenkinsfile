pipeline {
    agent any
    stages {
        stage ('Pull GitHub repository') {
            steps {
                git credentialsId: 'githubtoken', url: 'https://github.com/22127025/MMT_NC-Project3.git'
            }
        }
        stage ('Build and push DockerHub') {
            steps {
                withDockerRegistry(credentialsId: 'dockerhubtoken', url: 'https://index.docker.io/v1/') {
                    bat 'docker build -t 22127025/test-proj:latest .'
                    bat 'docker push 22127025/test-proj:latest'
                }
            }
        }
    }
}