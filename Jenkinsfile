pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                #! /bin/bash -p

                # List all subdirectories of the directory given in the first positional
                # parameter.  Include subdirectories whose names begin with dot.  Exclude
                # symlinks to directories.

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
