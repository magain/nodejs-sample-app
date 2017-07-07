node('testing') {
  stage('Init') {
    echo "Initializing ..."
  }
  stage('Checkout') {
    checkout scm
  }
/**
  *  stage('test') {
  *    steps {
  *      nodejs(nodeJSInstallationName: 'nodejs') {
  *        sh 'npm install --only=dev'
  *        sh 'npm test'
  *      }
  *    }
  *  }
  *  stage('docker build/push') {
  *    steps {
  *      docker.withRegistry('https://index.docker.io/v1/', 'dockerhub') {
  *        def app = docker.build("magain/nodejs-sample-app", '.').push()
  *      }
  *    }
  *  }
  **/
}
