pipeline {
    agent { label 'docker-agent-alpine' }

    stages {
        stage('Build') {
            steps {
                sh 'python3 helloworld.py'
            }
        }
    }
}
pipeline {
    agent { 
        node {
            label 'docker-agent-alpine'
            }
      }
    stages {
        stage('Build') {
            agent any
            steps {
                echo "Building.."
                sh '''
                echo "doing build stuff..",
                sh 'python3 helloworld.py'
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff..
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}