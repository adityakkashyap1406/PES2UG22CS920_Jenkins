pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                    g++ main.cpp -o PES2UG22CS920
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    ./PES2UG22CS920
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployed'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
