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
        sh 'make deploy-production-local'
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