pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/KartikeyD/DevOpsAssignment1.git'
            }
        }
        stage('Build') {
            steps {
                sh 'your-build-command'
            }
        }
        stage('Test') {
            steps {
                sh 'your-test-command'
            }
        }
    }
}
