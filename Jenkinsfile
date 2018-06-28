pipeline {
  agent {
    label 'build'
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
       //powershell 'docker run -v c:\\Users\\thomashillyer\\Documents\\JENKINSARCHTEST:c:\\sharedspace --name build thomashillyer/suite_build:latest'
       powershell 'docker run -d thomashillyer/suite_build:latest'
       //powershell 'winpty docker exec -it build powershell'
       powershell 'cd c:\\jenkins\\'
       powershell 'mkdir randomtest -force'
      }
    }
    
  }
  environment {
    CI = 'true'
  }
}
