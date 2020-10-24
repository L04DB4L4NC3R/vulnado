pipeline {
	agent any
	stages {
		stage("SonarQube") {
			 environment {
        scannerHome = tool 'SonarQube Scanner'
    }
			steps {
        withSonarQubeEnv ('SonarQube Scanner') {
			sh 'mvn -fn clean install sonar:sonar'
            sh '${scannerHome}/bin/sonar-scanner'
            sh 'cat .scannerwork/report-task.txt'
        }
    }
		}
	}
}
