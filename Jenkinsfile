pipeline {
    agent any

    environment {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/jodiac99/aws-cicd.git'
        IMAGE_TAG = jodiac99_awscicd
        IMAGE_VERSION = "${BUILD_NUMBER}"
    }
    stages {
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t "${IMAGE_TAG}:${IMAGE VERSION}" .'   
                sh 'docker images'
            }
        }
    }



}