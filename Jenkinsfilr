pipeline {
    agent any

    stages {
        stage('Github') {
            steps {
                echo 'checkout github'
            }
        }
        stage('build') {
            steps {
                echo 'Building application'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing application'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying application'
            }
        }
    }
}
