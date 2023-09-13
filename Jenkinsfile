// pipeline {
//   agent any
//   stages {
//     stage('Hello Message') {
//       steps {
//         echo 'WELCOME '
//       }
//     }

//     stage('JavaVersion') {
//       parallel {
//         stage('JavaVersion') {
//           steps {
//             sh '''java --version

// '''
//           }
//         }

//         stage('maven version') {
//           steps {
//             sh 'mvn -v'
//           }
//         }

//         stage('gitversion') {
//           steps {
//             sh 'git --version'
//           }
//         }


pipeline {
    agent any

    environment {
        KUBECONFIG = 'C:\\Users\\Users\\Poornima\\config'
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
                    // Use 'start' to run a command in the background on Windows
                    bat 'start kubectl --kubeconfig=${KUBECONFIG} apply -f deployment.yaml'
                    bat 'start kubectl --kubeconfig=${KUBECONFIG} apply -f service.yaml'
                }
            }
        }
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

      }
    }

 
