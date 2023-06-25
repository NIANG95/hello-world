pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('SCM') {
      steps {
        git 'https://github.com/NIANG95/hello-world.git'
      }
    }  
    stage('Build') {
      steps {
        withSonarQubeEnv(installationName: 'sonarqube-9.9.1'){
          sh './mvnw clear org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
        }
      }
    }
  }
}
