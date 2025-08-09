pipeline {
  agent any

  parameters {
    choice(
      name: 'ENVIRONMENT',
      choices: ['testing', 'stage'],
      description: 'Select the target environment'
    )
  }

  stages {
    stage('Build Image') {
      steps {
        sh """
          echo "Building for environment: ${params.ENVIRONMENT}"
          docker build . -t test:${params.ENVIRONMENT} --build-arg ENVIRONMENT=${params.ENVIRONMENT}
        """
      }
    }
  }
}

