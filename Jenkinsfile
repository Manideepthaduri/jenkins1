pipeline {
    agent any

    tools {
       maven 'maven-3.9.3'
    }

    stages {
        stage('git clone') {
            steps {
            bat git branch: 'main', url: 'https://github.com/Manideepthaduri/ks.git'
            }
        }
		stage('Maven Clean')
		{
		  steps {
		  bat 'mvn clean'
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
