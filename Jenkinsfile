pipeline {
  agent any
  triggers {
      pollSCM '* * * * *'
  }
  tools {
      maven 'M2_HOME'
  }
  stages {
    stage('build') {
      steps {
        sh 'mvn clean'
        sh 'mvn install'
        sh 'mvn package'
        sh 'mvn test'
      }  
    }
     stage ('deploy to tomcat') {
         steps {
           deploy adapters: [tomcat8(path: '', url: 'http://192.168.1.217:8080/')], contextPath: null, war: '**/*.war'
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
       echo "This is what I love from this pipeline"
       echo "Thi pipeline is sweet"
       sleep 10
      }  
    }
  }
}   
