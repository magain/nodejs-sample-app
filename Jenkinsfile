node {
  stage('Init') {
    echo 'Initializing ...'
  }
  stage('Checkout') {
    echo 'Getting source code ...'
    checkout scm
  }
  stage('nodejs test') {
    echo 'test nodejs via command npm --version'
    sh 'npm --version'
  }
}
