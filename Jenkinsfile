pipeline {
    agent any
    stages {
        stage ('Pull Github repository') {
            steps {
                git credentialsId: 'Github Token', url: 'https://github.com/22127025/MMT_NC-Project3.git'
            }
        }
        stage ('Build and push DockerHub') {
            steps {
                withDockerRegistry(credentialsId: 'Docker', url: 'https://index.docker.io/v1/') {
                    bat 'docker build -t 22127025/test-dockerhub:latest .'
                    bat 'docker push 22127025/test-dockerhub:latest'
                }
            }
        }
    }
}