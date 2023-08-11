pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/waseemshaik1993/spring-hello-app'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
