pipeline {
    agent any

    stages {
        stage('Checkout the repository') {
            steps {
                checkout scm
            }
        }
        stage('Install dependencies') {
            steps {
                bat 'npm install'
            }
        }


        stage('Test the code'){
            steps{
                bat 'npm run test'
            }
        }
    }

    post {
        always {
            echo 'Pipline completed'
        }
        success {
            echo 'Build succedded'
        }
        failure {
            echo 'Build failed'
        }
    }
}