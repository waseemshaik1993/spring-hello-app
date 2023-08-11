pipeline {
    agent any
    environment {
        app = 'springboot-frontend'
        SONAR_LOGIN = credentials('Sonar-Creds')
    }
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
        stage('Compile and Run Sonar Analysis') {
            steps {
                sh mvn clean verify sonar:sonar \
            -Dsonar.projectKey=Spring-Waseem \
            -Dsonar.projectName='Spring-Waseem' \
            -Dsonar.host.url=http://18.136.72.199:9000 \
            -Dsonar.token=sqp_0c985d7c5d47e41960e40f0ccf04723d2b1446be
            }
        }
    }
}
