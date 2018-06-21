pipeline {
  agent {
    label 'windows_agent_host'
  }
  stages {
    stage('Build') {
      //agent {
      //  docker { 
      //    image 'thomashillyer/suite_build:latest'
      //    args '-v C:\\Users\\thomashillyer\\Documents\\JENKINSARCHTEST:/jenkins/'
      //  }
      //}
      steps {
       powershell 'echo start'
       powershell 'cd c:\\jenkins\\'
       powershell 'mkdir randomtest'
      }
    }
    
  }
  environment {
    CI = 'true'
  }
}
