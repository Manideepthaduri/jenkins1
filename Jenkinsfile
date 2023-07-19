pipeline {
    agent any

    tools {
       maven 'maven-3.9.3'
    }

    stages {
        stage('git clone') {
            steps {
            git branch: 'main', url: 'https://github.com/Manideepthaduri/ks.git'
            }
        }
		stage('Maven Clean')
		{
		  steps {
		  bat 'mvn clean'
		  }
		}
		stage ('SonarQube Scan') {
		  steps {
          bat
		  mvnsonar:sonar \
		  -Dsonar.host.url=http://52.87.174.106:9000\-Dsonar.login=cec1830c5478df968ed004e57143377eba54daa1
		  }
		}
		stage('Maven Test')
		{
		  steps {
		  bat 'mvn test'
		  }
		}
		stage('Maven compile')
		{
		  steps {
		  bat 'mvn compile'
		  }
		}
				
		stage('Maven Package')
		{
		  steps {
		  bat 'mvn package'
		  }
		}
		stage('Maven Deploy')
		{
		  steps {
		  bat 'mvn deploy'
		  }
		}
	}
}
