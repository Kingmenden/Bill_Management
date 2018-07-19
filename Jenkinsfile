pipeline {
  agent any
  stages {
    stage('Maven Build') {
      steps {
        sh '''mvn clean package -DskipTests
'''
      }
    }
    stage('tomcat deploy') {
      steps {
        sh 'mvn tomcat7: deploy'
      }
    }
  }
}