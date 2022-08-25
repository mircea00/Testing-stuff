pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                'shopt -s dotglob'
                'shopt -s nullglob'
                'for d in "$1"/*/; do'
                'dir=${d%/}'                  
                '[[ -L $dir ]] && continue'
                'printf '%s\n' "$dir"'
                'done'
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
