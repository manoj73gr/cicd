pipeline {
    agent any

    stages {
        stage('Build docker image') {
            steps {
              sh 'sudo docker build . -t 469744164476.dkr.ecr.us-east-1.amazonaws.com/test:$BUILD_NUMBER'
              sh 'ls'
            }
        }
        stage('Login to ECR repo') {
            steps {
                
                sh 'sudo docker images'
            }
        }
        stage('Push docker image to ecr') {
            steps {
              sh ' sudo docker push 469744164476.dkr.ecr.us-east-1.amazonaws.com/test:$BUILD_NUMBER'
            }
        }
    }
}
