pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    
    }
    stage() {
      steps {
        sh 'mvn clean test'
        junit '**/target/*.xml'
      }
    }
  }
}
