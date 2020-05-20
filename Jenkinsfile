pipeline {
    agent {
        // docker {
        //     image 'node'
        //     args '-p 3000:3000'
        // }
        none
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}
