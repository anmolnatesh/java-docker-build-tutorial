def pom = readMavenPom file: 'pom.xml'
def version = pom.version
pipeline {
  agent any
  stages{
    stage('read'){
      steps{
      echo "hi"
      echo version
    }
  }
}
}


