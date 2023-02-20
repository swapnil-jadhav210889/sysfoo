pipeline {
  agent {
    docker {
      image 'maven:3.9.0-sapmachine-17'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        sh 'mvn package -DskipTests'
      }
    }

  }
  tools {
    maven 'Maven3.9.0'
  }
}