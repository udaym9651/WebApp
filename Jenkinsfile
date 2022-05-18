pipeline {
  stages {
    stage('Build') {
      agent any
      steps {
        sh 'mvn clean install'
      }
    
    }
    stage('Test') {
      agent {
        label 'agent'
      }
      steps {
        sh 'mvn clean test'
        junit '**/target/surefire-reports/*.xml'
      }
    }
  }
}
