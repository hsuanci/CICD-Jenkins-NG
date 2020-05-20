pipeline {
    agent any

    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                bat 'npm build'
            }
        }
        stage('Deploy') {
            steps {
                uploadToDefaultFTP('filePath')
            }
        }
    }
}
