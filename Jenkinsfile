pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ PES1UG22CS343.cpp -o error'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG22CS343-1'
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulating Deployment...'
                sh 'cp PES1UG22CS343-1 /tmp/'  // Example deploy step
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
