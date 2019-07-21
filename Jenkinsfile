node {  
    stage('Code Checkout') { 
        git credentialsId: 'githubID', url: 'https://github.com/itrainrainbow/maven_app.git' 
    }
    stage('Build') { 
        withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
        sh 'mvn clean compile'
      }
    }
    stage('Unit Test') { 
         withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
        sh 'mvn test'
      } 
    }
    stage('Package') { 
         withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.1') {
        sh 'mvn package'
      }  
    }
    stage('Deploy to Dev') { 
        // 
    }
    stage('Deploy to Stage') { 
        // 
    }
    stage('Deploy to Prod') { 
        // 
    }
}
