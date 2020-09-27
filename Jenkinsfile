pipeline {
    agent any

    stages {
        stage('Build docker image') {
            steps {
              sh 'docker build . -t 469744164476.dkr.ecr.us-east-1.amazonaws.com/test:$BUILD_NUMBER'
              sh 'ls'
            }
        }
        stage('List docker images') {
            steps {
                
                sh 'docker images'
            }
        }
        stage('Login to AWS ECR repo') {
            steps {
                
               sh '$(aws ecr get-login --no-include-email --region us-east-1)'
            }
        }
        stage('Push docker image to ecr') {
            steps {
              sh 'docker push 469744164476.dkr.ecr.us-east-1.amazonaws.com/test:$BUILD_NUMBER'
            }
        }
       stage('Kubernetes integration with jenkins ') {
            steps {
              sh 'kubectl get nodes'
            }
        }
       stage('Deploy to kubernetes ') {
            steps {
              sh 'ls'
              sh 'pwd'
              sh 'cd helmchart'
              sh 'ls'
              sh 'helm install mongodb ./expresscart/ --namespace mongodb'
            }
        }
    }
}
