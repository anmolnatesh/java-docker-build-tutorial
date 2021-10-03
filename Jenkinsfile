


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
        script{
          pom = readMavenPom(file: 'pom.xml')

            def pom_version = pom.version
        }
      }
  }
}
}


