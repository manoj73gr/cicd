pipeline {
    agent any

    stages {
        stage('Build docker image') {
            steps {
              sh 'docker build . -t 469744164476.dkr.ecr.us-east-1.amazonaws.com/test:$BUILD_NUMBER'
              sh 'ls'
            }
        }
        stage('Login to ECR repo') {
            steps {
                
                sh 'docker images'
            }
        }
        stage('Push docker image to ecr') {
            steps {
              sh 'docker push 469744164476.dkr.ecr.us-east-1.amazonaws.com/test:$BUILD_NUMBER'
            }
        }
    }
}
