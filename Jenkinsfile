pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                sh echo 'ls'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
