pipeline {
    agent any
    // parameters {
    //     choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
    //     booleanParam(name: 'executeTests', defaultValue: true, description: '')
    // }
    stages {
        // stage("Checkout") {
        //     steps {
        //         checkout scm
        //     }
        // }
        stage("Build") {
            steps {
                echo 'Building the application...'
                sh 'docker-compose build web'
            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                script {
                    gv.test()
                }
            }
        }
        stage("Deploy") {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}