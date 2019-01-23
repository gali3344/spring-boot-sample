pipeline {
  agent any
  stages {
    stage('ls') {
      steps {
        sh '''pwd & ls
'''
      }
    }
    stage('deploy') {
      steps {
        sh '''docker-compose run package
make build-docker-prod-image
make deploy-production-local
'''
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again!'
      sh 'docker-compose run clean'

    }

    success {
      echo 'success!'

    }

    failure {
      echo 'failure!'

    }

  }
}