pipeline {
    agent any
    environment {
        DOCKER_USER = 'mon-utilisateur-docker'
    }
    stages {
        stage('Login Docker') {
            steps {
                withCredentials([string(credentialsId: 'DOCKER_PASSWORD', variable: 'DOCKER_PASSWORD')]) {
                    sh 'echo $DOCKER_PASSWORD | docker login -u $DOCKER_USER --password-stdin'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    def buildVersion = "1.0.${env.BUILD_NUMBER}"
                    echo "Building ${APP_NAME} version ${buildVersion}"
                }
            }
        }
        stage('Test') {
            steps {
                echo "Testing ${APP_NAME}..."
            }
        }
        stage('Deploy') {
            steps {
                script {
                    def buildVersion = "1.0.${env.BUILD_NUMBER}"
                    echo "Deploying ${APP_NAME} version ${buildVersion}"
                }
            }
        }
    }
}