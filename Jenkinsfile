pipeline {
  agent any

  tools {
    maven 'Maven_3_5_2'
  }

  environment {
    SONAR_TOKEN = credentials('SONAR_TOKEN_ID') // store token in Jenkins credentials
  }

  stages {
    stage('Compile and Run Sonar Analysis') {
      steps {
        sh """
          mvn clean verify sonar:sonar \
            -Dsonar.projectKey=guruking \
            -Dsonar.organization=bernardking007 \
            -Dsonar.host.url=https://sonarcloud.io \
            -Dsonar.token=$SONAR_TOKEN
        """
      }
    }
  }
}
