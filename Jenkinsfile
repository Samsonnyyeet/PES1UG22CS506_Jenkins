pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS506-1'
                sh 'g++ working.cpp -o working'
            }
        }
        stage('Test') {
            steps {
                sh './working'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}