pipeline {
    agent any

    environment {
        IMAGE_NAME = "mywebsite"
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'test -f index.html'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging application...'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t $IMAGE_NAME:latest .'
            }
        }
    }
}
