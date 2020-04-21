pipeline {
    agent any
    stages {
        stage('Docker build') {
            steps {
                sh "docker build -t python-app:v3 ."
            }
        }
        stage('Docker run') {
            steps {
                sh "docker run -p 5000:5000 -d python-app:v3 ."
            }
        }
        stage('Webpage check') {
            steps {
                sh "curl http://0.0.0.0:5000/ "
            }
        }
    }
}
