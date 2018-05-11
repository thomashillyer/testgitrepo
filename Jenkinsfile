pipeline {
    agent {
		label 'Windows_Slave'
	}
	environment {
		CI = 'true'
	}
    stages {
        stage('Build') {
			steps {
				powershell 'echo Hello'
			}
        }
    }
}
