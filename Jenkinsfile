pipeline {
  agent any
  stages {
    stage('Hello Message') {
      steps {
        echo 'WELCOME '
      }
    }

    stage('JavaVersion') {
      parallel {
        stage('JavaVersion') {
          steps {
            sh '''java --version

'''
          }
        }

        stage('maven version') {
          steps {
            sh 'mvn -v'
          }
        }

        stage('gitversion') {
          steps {
            sh 'git --version'
          }
        }

      }
    }

  }
}