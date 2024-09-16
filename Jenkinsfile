pipeline {
    agent any

    stages {

        stage('checkout') {
             steps {
                echo 'checkout ..'
                checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git_cred', url: 'git@github.com:venugopalgotagi/learning.git']])
             }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sh './gradlew clean build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
