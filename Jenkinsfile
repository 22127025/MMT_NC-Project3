pipeline {
    agent any
    stages {
        stage ('Pull GitHub repository') {
            steps {
                git credentialsId: 'githubtoken', url: 'https://github.com/22127025/MMT_NC-Project3.git'
            }
        }
    }
}