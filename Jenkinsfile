pipeline {
  agent any
  stages {
    stage('Maven Build') {
      parallel {
        stage('Maven Build') {
          steps {
            sh '''mvn clean package -DskipTests
'''
          }
        }
        stage('start tomcat') {
          steps {
            sh 'sudo service tomcat start'
          }
        }
      }
    }
    stage('tomcat deploy') {
      steps {
        sh 'mvn tomcat7:deploy'
      }
    }
  }
}