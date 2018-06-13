pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            powershell 'echo Hello'
          }
        }
        stage('Approval') {
          steps {
            input(message: 'are you sure', ok: 'yes', submitter: 'thomas', submitterParameter: 'admin')
          }
        }
      }
    }
  }
  environment {
    CI = 'true'
  }
}