pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                sh 'cd ..'
                sh 'ls'
                sh 'sudo apt-get update'
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
                echo '-----------------Deleting workspace--------------'
                leanWs(cleanWhenNotBuilt: false,
                    deleteDirs: true,
                    disableDeferredWipeout: true,
                    notFailBuild: true,
                    patterns: [[pattern: '.gitignore', type: 'INCLUDE'],
                               [pattern: '.propsfile', type: 'EXCLUDE']])
            }
        }
    }
}



