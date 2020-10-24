pipeline {
	agent any
	stages {
		stage("SonarQube") {
			 environment {
        scannerHome = tool 'SonarQube Scanner'
    }
			steps {
				sh 'mvn -fn clean install sonar:sonar'
            	sh 'mvn sonar:sonar'
    }
		}
	}
}
