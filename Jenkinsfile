pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Harshithkiaq/Jenkins'
            }
        }
        stage('ls') {
            steps {
                sh '''ls
                      cat index.html'''
            }
            post {
                success {
                    archiveArtifacts artifacts: 'index.html'
                }
            }
        }
    }
}

