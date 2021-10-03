pipeline {
  agent any
  tools {
    maven 'm3'
  }
  environment {
    registry = "anmolnatesh/try"
    registryCredential = 'docker'
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
        mvn package
        ls target
        '''
      }
    }
    stage('docker')
    {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
    stage('Deploy Image') {
      steps{    script {
        docker.withRegistry( '', registryCredential ) {
        dockerImage.push()
      }
    }
  }
}
  }
}
