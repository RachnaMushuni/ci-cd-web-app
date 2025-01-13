pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'git@github.com:RachnaMushuni/ci-cd-web-app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t gcr.io/ci-cd-web-app/my-web-app:latest .'
            }
        }
        stage('Push to GCR') {
            steps {
                sh 'docker push gcr.io/ci-cd-web-app/my-web-app:latest'
            }
        }
    }
}
