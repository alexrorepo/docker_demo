pipeline {
    agent any

    stages {
        stage('Show workspace') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Build Docker image') {
            steps {
                sh 'docker build -t pytest-demo .'
            }
        }

        stage('Run pytest') {
            steps {
                sh 'docker run --rm pytest-demo'
            }
        }
    }
}