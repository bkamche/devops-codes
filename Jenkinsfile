pipeline {
  agent any
  tools {
      maven 'M2_HOME'
  }
  stages {
    stage('build'){
      steps {
        sh 'mv clean'
        sh 'mv install'
        sh 'mv package'
      }  
    }
     stage('test'){
      steps {
       echo "test step"
       sh 'mv test'
      }  
    }
     stage('deploy'){
      steps {
       echo "deploy step"
       sleep 10
      }  
    }
     stage('docker'){
      steps {
       echo "image step"
       sleep 10
      }  
    }
  }
}   
