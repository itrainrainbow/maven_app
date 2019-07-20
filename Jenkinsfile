node {
   stage('Code checkout') { // for display purposes
      // Get some code from a GitHub repository
      git credentialsId: 'githubID', url: 'https://github.com/itrainspartans/maven_app.git'
   }
   stage('Build') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
      sh 'mvn clean compile'
     } 
   }
   stage('Test') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
      sh 'mvn test'
     }  
   }
   stage('Sonar CodeAnalysis') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
             sh 'mvn clean verify sonar:sonar ' +
             ' -Dsonar.host.url=https://sonarcloud.io/ ' +
             ' -Dsonar.organization=itrainspartans '+ 
             ' -Dsonar.login=fe081245dcecb35f616d678b5dc61153533bdb18 '
                
       }
    }
   stage('Package') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
      sh 'mvn package'
     }  
   }
   
   
   stage('Artifactory') {
     
   }
   
   stage('Docker Build') {
     
   }
   
   stage('Deploy to Dev') {
     
   }
   stage('Deploy to Stage') {
     
   }
   stage('Deploy to Prod') {
     
   }
}
