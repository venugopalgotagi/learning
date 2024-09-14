pipeline {
    agent any

    stages {

        stage {
            checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[credentialsId: '5bdbf19e-a67c-46ec-adda-850785e6bb22', url: 'git@github.com:venugopalgotagi/learning.git']])
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