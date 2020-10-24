pipeline {
	agent any
	stages {
		stage("SonarQube") {
			steps {
				sh 'mvn -fn clean install sonar:sonar'
            	sh 'mvn sonar:sonar -Dsonar.projectKey=vnado -Dsonar.host.url=http://localhost:9000 -Dsonar.login=b8ef16f9ccd1f313861a903e0dec4d33e5cb0f4c'
    		}
		}
	}
}
