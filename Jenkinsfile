pipeline {
  agent any
  stages {
    stage('one') {
      steps {
        echo 'this is the build job'
        sh 'mvn compile'
      }
    }

    
    stage('two') {
      steps {
        echo 'this is the test job'
        sh 'mvn clean test'
      
      }
    }
    

    stage('three') {
      steps {
        echo 'this is the job for packaging'
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  
  tools {
    maven 'Maven 3.6.3'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}
