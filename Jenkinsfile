pipeline {
    agent any

    stages {
        stage('Git') {
            steps {
                git branch: 'main', credentialsId: 'github-signin', url: 'https://github.com/ikim318/jenkins_practice.git'
            }
        }

        stage('Build') {
            steps {
                sh 'python3 helloworld.py'
            }
        }
    }
}
