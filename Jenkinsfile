pipeline {
  agent any
  tools {
    nodejs 'Node 6.x'
  }
  stages {
    stage('Preparation') {
      checkout scm
    }
    stage('test') {
      nodejs(nodeJSInstallationName: 'nodejs') {
        sh 'npm install --only=dev'
        sh 'npm test'
      }
    }
    stage('docker build/push') {
      docker.withRegistry('https://index.docker.io/v1/', 'dockerhub') {
        def app = docker.build("magain/nodejs-sample-app, '.').push()
      }
    }
  }
}
