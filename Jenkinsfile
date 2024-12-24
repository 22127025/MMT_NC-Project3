pipeline {
    agent any
    stages {
        stage ('Pull Github repository') {
            steps {
                git credentialsId: 'Github Token', url: 'https://github.com/22127025/MMT_NC-Project3.git'
            }
        }
    }
}