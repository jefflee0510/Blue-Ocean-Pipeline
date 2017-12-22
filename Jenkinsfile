pipeline {
  agent any
  stages {
    stage('Initialize') {
      agent {
        docker {
          image 'maven:3.5.2-jdk-9'
          args '-v /Users/MTRMAC/Documents/apache-maven-3.5.2'
        }
        
      }
      steps {
        echo 'Add a minimal pipeline'
      }
    }
  }
}