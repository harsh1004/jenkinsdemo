pipeline {
  agent any
  stages {
    stage('user-input') {
    def userInput = input(
   id: 'userInput', message: 'Let\'s promote?', parameters: [
   [$class: 'TextParameterDefinition', defaultValue: 'service', description: 'services to be built', name: 'service_name'],
   [$class: 'TextParameterDefinition', defaultValue: 'master', description: 'branch to be built', name: 'branch']
])
echo ("service_name: "+userInput['service_name'])
echo ("branch: "+userInput['branch'])

    }
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
