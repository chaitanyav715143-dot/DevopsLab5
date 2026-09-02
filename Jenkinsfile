pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'javac Put.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java Put'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }
}
