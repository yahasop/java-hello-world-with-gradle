node ('built-in') {
  tools{
      gradle 'gradle-jenkins'
  }

  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    withSonarQubeEnv() {
      sh "./gradlew sonar"
    }
  }
}