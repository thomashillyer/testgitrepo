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
        powershell 'docker version'
        powershell 'docker run hello-world'
       powershell 'docker run -v c:\\Users\\thomashillyer\\Documents\\JENKINSARCHTEST:\\jenkins --name build thomashillyer/suite_build:latest'
       powershell 'docker exec -it build powershell'
       powershell 'cd c:\\jenkins\\'
       powershell 'mkdir randomtest -force'
      }
    }
    
  }
  environment {
    CI = 'true'
  }
}
