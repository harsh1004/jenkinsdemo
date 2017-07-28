pipeline {
  agent any
  stages {
    stage('build-service') {
      steps {
        build 'Dev.eng-idm.service-service' parameters: [string(name: 'branch_name', value: 'testforjenkins1')]
        build 'Dev.eng-idm.service-service' parameters: [string(name: 'branch_name', value: 'testforjenkins')]
      }
    }
  }
  environment {
    APPLICATION_NAME = 'abc'
  }
}
