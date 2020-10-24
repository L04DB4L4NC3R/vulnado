pipeline {
	agent any
	stages {
		stage("sonarqube") {
			 environment {
        scannerHome = tool 'SonarQube Scanner'
    }
			steps {
        withSonarQubeEnv ('sonarqube') {
            sh '${scannerHome}/bin/sonar-scanner'
            sh 'cat .scannerwork/report-task.txt'
        }
    }
		}
	}
}
