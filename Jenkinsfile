pipeline {
    agent any
    stages {
        stage('Check Branch') {
            when {
                branch 'develop'
            }
            steps {
                echo "Hello from develop branch"
            }
        }
    }
}
