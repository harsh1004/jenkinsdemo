pipeline {
  agent any
  stages {
    stage('build-service') {
      steps {
        build 'Dev.eng-idm.service-service'
      }
    }
  }
  environment {
    APPLICATION_NAME = 'abc'
  }
}