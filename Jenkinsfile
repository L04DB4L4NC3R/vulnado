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
            sh 'mvn sonar:sonar -Dsonar.projectKey=dvja -Dsonar.host.url=http://localhost:9000 -Dsonar.login=780849ad0f3edb13b2cacdb4c79954132dd78115'
			sh 'cat .scannerwork/report-task.txt'
        }
    }
		}
	}
}
