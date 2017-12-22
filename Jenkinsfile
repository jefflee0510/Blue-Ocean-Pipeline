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
        sh '''echo PATH = ${PATH}
echo M2_HOME = ${M2_HOME}
mvn clean'''
      }
    }
    stage('Build') {
      steps {
        sh 'mvn -Dmaven.test.failure.ignore=true install'
      }
    }
    stage('Report') {
      steps {
        dependencyCheckPublisher()
      }
    }
  }
}