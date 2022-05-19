pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
        archiveArtifacts artifacts: '**/target/*.jar'
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
