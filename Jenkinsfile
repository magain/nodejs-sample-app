node {
  stage('Init') {
    echo 'Initializing ...'
  }
  stage('Checkout') {
    echo 'Getting source code ...'
    checkout scm
  }
  stage('nodejs test') {
    sh 'npm --version'
  }
}
