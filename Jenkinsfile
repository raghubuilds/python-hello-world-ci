pipeline {
    agent any
    stages {
        stage('Docker build') {
            steps {
                sh "docker build -t python-app:v3 ."
            }
        }
    }
}
