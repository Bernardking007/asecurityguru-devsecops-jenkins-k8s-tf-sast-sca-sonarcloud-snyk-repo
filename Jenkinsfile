pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=guruking -Dsonar.organization=bernardking007-Dsonar.host.url=https://sonarcloud.io -Dsonar.token=7df9f3e35c17dd4a23a0cad05de506702f7ec124
			}
    }
    }		
  }
}
