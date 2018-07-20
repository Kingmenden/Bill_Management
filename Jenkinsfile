pipeline {
  agent any
  stages {
    stage('mvn build') {
      parallel {
        stage('mvn build') {
          steps {
            sh 'mvn clean package -DskipTests'
          }
        }
        stage('start Tomcat') {
          steps {
            sh 'sudo service tomcat start'
          }
        }
      }
    }
    stage('Tomcat Deploy') {
      steps {
        sh 'mvn tomcat7: deploy'
      }
    }
  }
}