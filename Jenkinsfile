pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building...'
          }
        }
        stage('Approval') {
          steps {
            input(message: 'Approve?', ok: 'Approve', submitter: 'thomashillyer', submitterParameter: 'admin')
          }
        }
        stage('Email') {
          steps {
            echo 'Email Sent'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
  environment {
    CI = 'true'
  }
}