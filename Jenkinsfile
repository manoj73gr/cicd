pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              sh 'sudo docker build . -t test:latest'
              sh 'ls'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
