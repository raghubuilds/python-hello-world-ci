pipeline {
    agent any
    stages {
        stage('Docker build') {
            steps {
                sh "docker build -t python-app:v5 ."
            }
        }
        stage('Docker run') {
            steps {
                sh "docker run --rm -it -p 5000:5000 -d python-app:v5 sleep 1000"
            }
        }
        stage('Webpage check') {
            steps {
                sh "curl http://0.0.0.0:5000/ "
            }
        }
    }
}
