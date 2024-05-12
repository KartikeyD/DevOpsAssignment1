pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], userRemoteConfigs: [[url: 'https://github.com/KartikeyD/DevOpsAssignment1.git']]])
            }
        }
        stage('Build') {
            steps {
                script {
                    try {
                        bat 'mvn clean package'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        throw e
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    try {
                        bat 'mvn test'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        throw e
                    }
                }
            }
        }
    }
}

