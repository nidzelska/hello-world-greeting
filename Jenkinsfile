node('master') {
  stage('Poll') {
    checkout scm
   }
   stage('Build and Unit test') {
     sh 'mvn clean verify -DskipITs=true';
     junit '**/target/superfire-reports/TEST-*.xml'
     archive 'target/*.jar'
   }
   stage('Integration Test'){
      sh 'mnv clean veriry -Dsurefire.skip=true';
      junit '**/target/failsafe-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
  }
   
   
   
   
