pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh 'whoami' // Runs on the Jenkins agent
            }
        }
        stage('Run inside Docker') {
            agent {
                docker {
                    image 'node:14' // Runs only this stage inside a Node.js 14 container
                }
            }
            steps {
                sh 'node -v' // Executes inside the container
            }
        }
    }
}
