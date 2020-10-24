pipeline {
	agent any
	stages {
		stage("sonarqube") {
			 environment {
        scannerHome = tool 'SonarQube Scanner'
    }
			steps {
        withSonarQubeEnv ('SonarQube') {
            sh '${scannerHome}/bin/sonar-scanner'
            sh 'cat .scannerwork/report-task.txt > /{JENKINS HOME DIRECTORY}/reports/sonarqube-report'
        }
    }
		}
	}
}
