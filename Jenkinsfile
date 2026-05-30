pipeline {

    agent any

    stages {

        stage('Build Project') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Package Project') {
            steps {
                bat 'mvn package'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -jar target/jenkinsProject3-1.0-SNAPSHOT.jar'
            }
        }

        stage('Show Target Folder') {
            steps {
                bat 'dir target'
            }
        }
    }

    post {

        success {
            echo 'CI/CD Pipeline Executed Successfully'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }
}