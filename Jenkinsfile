pipeline {
  agent any
  stages {
    stage('Hello Message') {
      steps {
        echo 'WELCOME '
      }
    }

    stage('JavaVersion') {
      steps {
        sh '''java --version
mvn -v
git --version
'''
      }
    }

  }
}