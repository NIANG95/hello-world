pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git 'https://github.com/NIANG95/hello-world.git'
      }
    }
    stage('Build'){
        steps{
        sh 'mvn clean package'
      }
    }
    stage('SonarQube analysis') {
      steps {
        withSonarQubeEnv(installationName: 'sonarqube-9.9.1'){
          sh "mvn sonar:sonar"
        }
      }
    }
  }
}
