pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Deploy to Minikube') {
      steps {
        script {
          bat 'start kubectl --kubeconfig=${KUBECONFIG} apply -f deployment.yaml'
          bat 'start kubectl --kubeconfig=${KUBECONFIG} apply -f service.yaml'
        }

      }
    }

  }
  environment {
    KUBECONFIG = 'C:\\Users\\Users\\Poornima\\config'
  }
  post {
    success {
      echo 'Deployment successful!'
    }

    failure {
      echo 'Deployment failed!'
    }

  }
}