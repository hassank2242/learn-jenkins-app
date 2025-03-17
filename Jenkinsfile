pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:14'
                    reuseNode true // Reuses the same workspace
                }
            }
            steps {
                sh '''
                node -v
                npm ci
                npm run build
                ls -la
                '''
            }
        }

        stage('Test') {
            agent {
                docker {
                    image 'node:14'
                    reuseNode true // Reuses the same workspace
                }
            }
            steps {
                sh '''
                node -v
                ls -la
                '''
            }
        }
    }
}
