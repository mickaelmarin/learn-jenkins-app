pipeline {
    agent any
    stages {
        stage('docker test') {
            agent {
                docker { 
                    image 'node:18-alpine' 
                    reuseNode true
                }
            }
            steps {
                sh 'npm --version >> npmversion.txt'
            }
        }
        stage('local workspace') {
            steps {
                sh 'touch toto.txt'
            }
        }
    }
}
