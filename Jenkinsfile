pipeline {
	agent any
	stages {
		stage("SonarQube") {
			steps {
				sh 'mvn -fn clean install sonar:sonar'
            	sh 'mvn sonar:sonar'
    		}
		}
	}
}
