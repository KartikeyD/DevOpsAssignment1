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
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
