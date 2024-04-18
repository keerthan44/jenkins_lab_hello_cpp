pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                build 'PES1UG21CS273-1'
                sh 'g++ hello.cpp -o output'
                echo 'Build Successful'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './output'
                echo 'Test Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                echo 'Deployment Successful'
            }
        }
    }
        post {
            failure {
                echo 'Pipeline Failed'
            }
            always {
                echo 'Pipeline execution completed.'
            }
        }
}
