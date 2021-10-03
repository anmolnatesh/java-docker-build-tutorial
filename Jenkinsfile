


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
            def mavenPom = readMavenPom file: 'pom.xml'
            
         }

       
      }
  }
}
}


