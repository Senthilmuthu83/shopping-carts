pipeline {
  agent any
  stages {
    stage('compile-app') {
      steps {
        echo 'this is the compile job'
        sh 'mvn compile'
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the second job'
        sh 'mvn test'
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the third job'
        sh 'mvn package'
      }
    }

    stage('archive-app') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}