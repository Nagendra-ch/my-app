node {
  stage('SCM') {
    git 'https://github.com/Nagendra-ch/my-app.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv(credentialsId: 'b6ba01fd-60a3-438e-8920-4db0b9119fa8', installationName: 'sonarqube') { // You can override the credential to be used
     //sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
	  sh 'mvn sonar:sonar \
  -Dsonar.projectKey=my-app \
  -Dsonar.host.url=http://192.168.56.109:9000 \
  -Dsonar.login=8dacca65a6eae445071ccae9cf7ba07cc51c5569'
	}
  }
}