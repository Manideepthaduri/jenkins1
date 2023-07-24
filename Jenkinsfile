pipeline {
    agent any

    tools {
       maven 'Maven 3.9.3'
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
		  sh '''mvn clean'''
		  }
		}
		stage('Maven Test')
		{
		  steps {
		  sh '''mvn test'''
		  }
		}
		stage('Maven compile')
		{
		  steps {
		  sh '''mvn compile'''
		  }
		}
				
		stage('Maven Package')
		{
		  steps {
		  sh '''mvn package'''
		  }
		}
		stage('Maven Deploy')
		{
		  steps {
		  sh '''mvn deploy'''
		  }
		}
	}
}
