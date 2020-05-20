pipeline {
    agent {
    }
    stages {
        stage('Restore') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm build'
            }
        }
    }
}