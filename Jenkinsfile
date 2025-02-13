pipeline {
    agent { label 'docker-agent-alpine' }

    stages {
        stage('Git') {
            steps {
                git branch: 'main', credentialsId: 'github-signin', url: 'https://github.com/ikim318/jenkins_practice.git'
            }
        }

        stage('Build') {
            agent docker { image 'python:3.11.7-alpine3.19' }
            steps {
                sh 'python3 helloworld.py'
            }
        }
    }
}
