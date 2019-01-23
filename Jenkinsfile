pipeline {
  agent any
  stages {
    stage('run test') {
      steps {
        sh 'docker-compose run test'
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