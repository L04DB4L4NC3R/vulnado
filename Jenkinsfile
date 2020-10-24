pipeline {
	agent any
	stages {
		stage("clean") {
			steps {
				sh 'mvn -fn clean install sonar:sonar'
			}
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
