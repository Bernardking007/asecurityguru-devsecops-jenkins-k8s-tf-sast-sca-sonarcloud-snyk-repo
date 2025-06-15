pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=guruking -Dsonar.organization=bernardking007-Dsonar.host.url=https://sonarcloud.io -Dsonar.token=226006e239f529fbcb12cf70d87d25ebb4e3ae28
			}
    }
    }		
  }
}
