@Library('gcloud-utils') _
pipeline {
    agent any 
    environment {
        GOOGLE_APPLICATION_CREDENTIALS = credentials('google_application_credentials')
    }
    stages {
        stage('Terraform Init') {
            steps {
                script {
                    sh 'echo 123'
                }
            }
        }
    }
}