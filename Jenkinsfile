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
                sh 'javac -d . src/*.java'
            }
        }
        stage('Test') {
            steps {
                sh 'java -cp . Main'
            }
        }
    }
}
