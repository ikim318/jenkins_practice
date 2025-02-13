pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }

    triggers {
      pollSCM '*/2 * * * *'
    }

    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                python3 helloworld.py
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy....'
                sh '''
                echo "doing deploy stuff.."
                '''
            }
        }
    }
}