node {
  stage('SCM') {
    git 'https://github.com/Nagendra-ch/my-app.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv(credentialsId: 'b6ba01fd-60a3-438e-8920-4db0b9119fa8', installationName: 'sonarqube') { // You can override the credential to be used
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
    }
  }
}
