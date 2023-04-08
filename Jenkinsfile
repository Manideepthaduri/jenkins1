node {
    stage('git clone') { 
	git branch: 'main', url: 'https://github.com/Manideepthaduri/ks.git'
    }
    stage('maven clean') {
	  bat 'mvn clean'
    }
    stage('maven validate') {
	  bat 'mvn validate'
    }
    stage('maven compile') {
	  bat 'mvn compile'
    }
    stage('maven test') {
	  bat 'mvn test'
    }
    stage('maven package') {
	  bat 'mvn package'
    }
    stage('maven deployment') {
	  bat 'mvn deploy'
	}
  }
   
     
