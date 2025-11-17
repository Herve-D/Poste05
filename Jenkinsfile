pipeline {
    agent any
 
    stages {
 
        stage('Build') { steps { echo "Build de la branche ${env.BRANCH_NAME}" }
        }
 
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
 
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
