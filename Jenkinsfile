pipeline {
    agent { 
        node {
            label 'docker-agent-alpine'
            }
      }

    triggers {
      pollSCM '* * * * *'
    }

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'python:3.11-alpine'
                }
            }
            steps {
                echo "Building.."
                sh '''
                cd myapp
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                cd myapp
                python3 hello.py
                python3 hello.py --name=Jenkins
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