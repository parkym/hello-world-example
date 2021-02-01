pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'mvn clean install'
      }
    }

    stage('Results') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
        archiveArtifacts 'target/*.jar'
      }
    }

  }
}