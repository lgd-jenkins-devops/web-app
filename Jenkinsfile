@Library('gcloud-utils') _
pipeline {
    agent any 
    environment {
        GOOGLE_APPLICATION_CREDENTIALS = credentials('google_application_credentials')
        BUCKET_NAME = credentials('web-app-bucket-name')
    }
    stages {
        stage('Terraform Init') {
            steps {
                script {
                    uploadToBucket("index.html",env.BUCKET_NAME)
                }
            }
        }
    }
}