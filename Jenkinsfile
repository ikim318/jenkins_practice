pipeline {
    agent { label 'docker-agent-alpine' }

    stages {
        stage('Build') {
            agent any
            steps {
                sh 'python3 helloworld.py'
            }
        }
    }
}
