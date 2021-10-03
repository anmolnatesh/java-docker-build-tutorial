pom = readMavenPom(file: 'pom.xml')


pipeline {
  agent any
  stages{
    stage('git') {
      steps{
        checkout scm
          }
    }
    stage('read'){
      steps{
      echo "hi"
      }
  }
}
}


