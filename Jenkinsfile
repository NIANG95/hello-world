pipeline {
  agent any
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'sonarqube-9.9.1') { 
          bat 'mvn clean sonar:sonar'
        }
      }
    }
  }
}
