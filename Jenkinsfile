pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                sg 'cd ..'
                sh 'ls'
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
