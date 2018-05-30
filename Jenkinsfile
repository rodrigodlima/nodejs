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
              sh 'npm i mocha'
              sh 'for i in $(find -name "*.js" -not -path "./node_modules/*"); do ./node_modules/.bin/mocha $i; done'
          }
      }
  }
}
