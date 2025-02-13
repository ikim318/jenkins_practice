pipeline {
    agent { 
        docker {
            image 'ikim318/jenkins-agent:python'
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
                python3 --verison
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