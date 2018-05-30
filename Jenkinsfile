pipeline {
  agent any
  stages {
      stage('Build') {
          steps {
              echo "Generate node_modules"
              sh 'npm i'
          }
      }
      stage('test') {
          steps {
              echo "Install Mocha and test code"
              sh 'sudo npm i -g mocha'
              sh './node_modules/.bin/mocha .'
          }
      }
  }
}
