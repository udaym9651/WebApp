pipeline {
  agent none
  stages {
    stage('Build') {
      agent any
      steps {
        sh 'mvn clean package'
        archiveArtifacts artifacts: '**/target/*.jar'
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
