pipeline {
  agent any
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'sonarqube-9.9.1') { 
          sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
        }
      }
    }
  }
}
