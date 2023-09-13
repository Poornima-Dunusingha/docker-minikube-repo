pipeline {
  agent any
  environment {
    KUBECONFIG = 'C:\\Users\\Poornima\\.kube\\config'
  }
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Deploy to Minikube') {
      steps {
        script {
          bat 'kubectl apply -f deployment.yaml'
          bat 'kubectl apply -f service.yaml'
        }

      }
    }

  }
  environment {
    KUBECONFIG = 'C:\\Users\\Poornima\\.kube\\config'
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
