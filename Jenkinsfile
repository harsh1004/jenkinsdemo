pipeline {
  agent any
  stages {
    stage('build-service') {
      steps {
        build job: 'Dev.eng-idm.user-service', parameters: [string(name: 'branch_name', value: 'testforjenkins1')]
        build job:'Dev.eng-idm.user-service', parameters: [string(name: 'branch_name', value: 'testforjenkins')]
      }
    }
  }
  environment {
    APPLICATION_NAME = 'abc'
  }
}
