pipeline {
    agent {
        agent { docker { image 'node' } }
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
