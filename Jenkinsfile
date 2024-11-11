@Library('gcloud-utils') _
pipeline {
    agent any 
    environment {
        GOOGLE_APPLICATION_CREDENTIALS = credentials('gcp-jenkins-deploy')
        BUCKET_NAME = credentials('web-app-bucket-name')
    }
    stages {
        stage('Update the web pages') {
            steps {
                script {
                    upload.uploadToBucket("src/*",env.BUCKET_NAME)
                }
            }
        }
    }
}