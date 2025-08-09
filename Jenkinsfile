pipeline {
    agent any
    stages {
        stage('Check Branch') {
            steps {
                sh "docker build . -t test"
            }
        }
    }
}

