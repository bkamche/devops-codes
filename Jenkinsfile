pipeline {
  agent any
  tools {
      maven 'M2_HOME'
  }
  stages {
    stage('build'){
      steps {
        sh 'mvn clean'
        sh 'mvn install'
        sh 'mvn package'
      }  
    }
     stage('test'){
      steps {
       echo "test step"
       sh 'mvn test'
      }  
    }
     stage('deploy'){
      steps {
       echo "deploy step"
       sleep 10
      }  
    }
     stage('CI/CD'){
      steps {
       echo "I love this pipeline CI/CI"
       sleep 10
      }  
    }
  }
}   
