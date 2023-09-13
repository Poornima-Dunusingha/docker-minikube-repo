pipeline {
  agent any
  stages {
    stage('Version Check') {
      steps {
        sh '''java -version
mvn -v
git --version
'''
      }
    }

  }
}