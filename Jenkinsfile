pipeline {
  agent any
  tools {
    maven 'm3'
  }
  environment {
    registry = "anmolnatesh/try"
    registryCredential = 'docker'
  stages {
    stage('git') {
      steps{
        checkout scm
          }
    }
    stage('build') {
      steps{
        sh '''
        mvn clean package
        ls target
        '''
      }
    }
    stage('docker')
    {
     
      steps{
        docker.build registry + ":$BUILD_NUMBER"

        
      }
    }
  }
}
