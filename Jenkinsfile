pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage("Build") {
            steps {
                echo 'building the application ...'
                echo "building version ${NEW_VERSION}"
            }
        }
        stage("Test") {
            steps {
                echo 'testing the application ...'
            }
        }
        stage("Deploy") {
            steps {
                echo 'deploying the application ...'
            }
        }
    }
    post {
        always {
            echo 'building..'
        }
        success {
            echo 'success'
        }
        failure {
            echo 'failure'
        }
    }
}