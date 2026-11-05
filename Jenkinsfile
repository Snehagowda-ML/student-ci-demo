
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Snehagowda-ML/student-ci-demo.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
