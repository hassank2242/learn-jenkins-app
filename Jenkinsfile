pipeline {
    agent any

    stages {
        
        stage('Build') {
            agent {
                docker {
                    image 'node:14' // Runs only this stage inside a Node.js 14 container
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
                    image 'node:14' // Runs only this stage inside a Node.js 14 container
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
