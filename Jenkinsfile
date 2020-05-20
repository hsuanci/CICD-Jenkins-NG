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
                 ftpPublisher alwaysPublishFromMaster: true,
                 continueOnError: false,
                 failOnError: false,
                 masterNodeName: '',
                 paramPublish: null,
                 publishers: [[configName: 'henryho', transfers: [[asciiMode: false, cleanRemote: true, excludes: '', flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: 'dist', sourceFiles: 'dist/jenkins-sample/*']], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false]]
            }
        }
    }
}
