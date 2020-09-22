pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh ""
                    docker build . test:latest
                sh ""
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
