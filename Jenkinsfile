pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                shopt -s dotglob
                shopt -s nullglob
                for d in "$1"/*/; do
                dir=${d%/}                  # Remove trailing slash
                [[ -L $dir ]] && continue   # Skip symlinks
                printf '%s\n' "$dir"
                done
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
