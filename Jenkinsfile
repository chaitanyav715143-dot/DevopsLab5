pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'javac Get.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java Get'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }
}
