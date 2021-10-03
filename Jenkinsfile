def version = sh script: 'mvn help:evaluate -Dexpression=project.version -q -DforceStdout', returnStdout: true
pipeline {
  agent any
  tools {
    maven 'm3'
  }
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
        echo ${version}
        
      }
    }
  }
}
