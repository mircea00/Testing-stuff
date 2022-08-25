pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                sh 'cd ..'
                sh 'ls'
                sh 'ls -l /var/jenkins_home/workspace'
                sh 'ls -l $WORKSPACE'
                sh 'ls -l /usr/bin'
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
