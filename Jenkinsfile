
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
      script{
        def mavenPom = readMavenPom file: 'pom.xml'
        def version  = mavenPom.version
      }

      echo "hi"
              
      }
  }
}
}


