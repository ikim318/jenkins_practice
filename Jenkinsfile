pipeline {
    agent { 
        node {
            label 'docker-agent-alpine'
            }
      }

    // triggers {
    //   pollSCM '*/5 * * * *'
    // }

    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd myapp
                pip3 install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
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