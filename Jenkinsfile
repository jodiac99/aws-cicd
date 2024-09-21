pipeline {
    agent any

    env {
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/jodiac99/aws-cicd.git'
    }
    stages {
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t aws-cicd .'
                sh 'docker images'
            }
        }
    }



}