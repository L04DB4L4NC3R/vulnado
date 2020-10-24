pipeline {
	agent any
	stages {
		stage("clean") {
			"mvn clean install sonar:sonar"
		}
		stage("SonarQube") {
			 environment {
        scannerHome = tool 'SonarQube Scanner'
    }
			steps {
        withSonarQubeEnv ('SonarQube Scanner') {
            sh '${scannerHome}/bin/sonar-scanner'
            sh 'cat .scannerwork/report-task.txt'
        }
    }
		}
	}
}
