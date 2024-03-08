pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG21CS184-1'
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './non_existent_executable'
                }
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
            error 'Pipeline failed'
        }
    }
}
