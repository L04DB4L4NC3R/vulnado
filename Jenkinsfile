pipeline {
	agent any
	stages {
		stage("SonarQube") {
			 environment {
        scannerHome = tool 'SonarQube Scanner'
    }
			steps {
			sh 'mvn -fn clean install sonar:sonar'
            sh 'mvn sonar:sonar -Dsonar.projectKey=wasdasdas -Dsonar.host.url=http://localhost:9000 -Dsonar.login=6718bff887d5218b6e4b2f87fc232cd86284dbb8'
    }
		}
	}
}
