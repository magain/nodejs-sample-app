pipeline {
  agent any
//  tools {
//    nodejs 'NodeJS 8.1.3'
//  }
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
//    stage('nodejs test') {
//      steps {
//        echo 'test nodejs via command npm --version'
//        nodejs(nodeJSInstallationName: 'nodejs', configId: '') {
//          sh 'npm --version'
//        }
//      }
//    }
    stage('Test') {
      steps {
        echo 'Create node container, install npm and execute tests'
        script {
          def myTestContainer = docker.image('node:8.1')
          myTestContainer.pull()
          myTestContainer.inside {
            sh 'npm install --only=dev'
            sh 'npm test'
          }
        }
      }
    }
  }
}
