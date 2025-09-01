pipeline {
    agent {
        node {
            label 'linux-node'
        }
    }

    stages {
        stage('Build') {
            steps {
                // Docker Build
                sh 'docker build . -t node-webapp'

                // Docker Run
                sh 'docker run -d -p 3000:3000 node-webapp'
            }
        }
    }
}
