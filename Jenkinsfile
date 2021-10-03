
pipeline {
  agent any
  tools {
    maven 'm3'
  }
  environment {
    //Use Pipeline Utility Steps plugin to read information from pom.xml into env variables
    IMAGE = readMavenPom().getArtifactId()
    VERSION = readMavenPom().getVersion()
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
        echo VERSION
        
      }
    }
  }
}
