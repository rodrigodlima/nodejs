pipeline {
  agent any
  stages {
      stage('Build') {
          steps {
              echo "Building dependencies"
              sh 'npm i'
          }
      }
      stage('test') {
          steps {
              echo "Install Mocha and test code"
              sh 'npm i -g mocha'
              sh './node_modules/.bin/mocha .'      
          }
      }
  }
}
