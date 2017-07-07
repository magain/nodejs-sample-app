pipeline {
  agent any
  tools {
    nodejs 'Node 8.x'
  }
  stages {
    stage('Init') {
      steps {
        echo 'Initializing ...'
      }
    }
    stage('Checkout') {
      steps {
        echo 'Getting source code ...'
        checkout scm
      }
    }
    stage('nodejs test') {
      steps {
        echo 'test nodejs via command npm --version'
        sh 'npm --version'
      }
    }
  }
}
