pipeline {
  agent { node { label 'workstation' } }

  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
        withAWSParameterStore(credentialsId: '', naming: 'basename', path: '/service', recursive: true, regionName: 'us-east-1') {
          sh 'env'
        }
      }
    }
  }
}

