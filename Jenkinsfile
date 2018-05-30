pipeline {
  agent any
  stages {
      stage('test') {
          steps {
              echo "test pipeline"
              sh npm install
              sh npm install mocha
              for i in $(find -name "*.js" -not -path "./node_modules/*"); do ./node_modules/.bin/mocha $i; done
              sh sleep 5
              sh tar zcvf projeto.tgz --exclude=./.git/ *
          }
      }
  }
}
