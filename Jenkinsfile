pipeline {

    agent any

    environment {
        IMAGE_NAME = 'myapp'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

      /*  stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t ${IMAGE_NAME}:latest .'
            }
        }

        stage('Docker Run') {
            steps {
                sh '''
                    docker stop ${IMAGE_NAME} || true
                    docker rm ${IMAGE_NAME} || true

                    docker run -d \
                        --name ${IMAGE_NAME} \
                        -p 8081:8080 \
                        ${IMAGE_NAME}:latest
                '''
            }
        } */
    }
}

