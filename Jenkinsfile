pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {

                echo 'testing'
            }
        }
    }
    post {
        success {
            echo 'test 1 success'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
