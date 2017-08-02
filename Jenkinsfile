#!/usr/bin/env groovy 
@Grab('org.apache.httpcomponents:httpclient:4.2.6')

def userInput = input(
   id: 'userInput', message: 'Let\'s promote?', parameters: [
   [$class: 'TextParameterDefinition', defaultValue: 'service', description: 'services to be built', name: 'service_name'],
   [$class: 'TextParameterDefinition', defaultValue: 'master', description: 'branch to be built', name: 'branch']
])
echo ("service_name: "+userInput['service_name'])
//@NonCPS def entries(service_name) {service_name.collect {k, v -> [k, v]}}

//echo(userInput['service_name'].values())
echo ("branch: "+userInput['branch'])



pipeline {
  agent any
  
   

 stages {
   stage('build-service') {
      steps {
        build job: 'Dev.eng-idm.user-service', parameters: [string(name: 'branch_name', value: userInput['branch'])]
        build job:'Dev.eng-idm.user-service', parameters: [string(name: 'branch_name', value: userInput['branch'])]
      }
    }
  }
  environment {
    APPLICATION_NAME = 'abc'
  }
}
