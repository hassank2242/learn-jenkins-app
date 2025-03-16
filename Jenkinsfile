pipeline {
    agent {
        docker {
            image 'node:14' // Runs the pipeline in a Node.js 14 container
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'node -v' // Runs inside the container
            }
        }
    }
}
