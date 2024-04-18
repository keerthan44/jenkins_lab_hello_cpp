pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'g++ hello.cp -o output'
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
