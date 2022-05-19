pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    
    }
    stage('Test') {
      steps {
        sh 'mvn clean test'
        junit '**/target/surefire-reports/*.xml'
      }
    }
  }
}
