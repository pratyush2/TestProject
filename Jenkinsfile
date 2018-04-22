node {
   
   stage('SCM Checkout') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/pratyush2/TestProject.git'
     
   }
   stage('Maven Build') {
    echo 'Build is started'
      withMaven(jdk: 'jdk 1.8', maven: 'maven 3.5.3') {
         sh 'mvn clean compile package '
      }
   }
   stage('Test Execution') {
    echo 'Test is executed' 
      withMaven(jdk: 'jdk 1.8', maven: 'maven 3.5.3') {
         sh 'mvn test package'
      }
   }
}
