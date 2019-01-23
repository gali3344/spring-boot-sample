pipeline {
  agent any
  stages {
    stage('ls') {
      steps {
        sh '''pwd & ls
'''
      }
    }
    stage('test') {
      steps {
        sh 'sudo docker-compose run test'
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