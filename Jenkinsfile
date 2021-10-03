
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
        sh '''
        docker login -u anmol -p $d1_PWD

        
      }
    }
  }
}
