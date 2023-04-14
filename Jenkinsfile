node {
    stage('git clone') { 
	git branch: 'main', url: 'https://github.com/Manideepthaduri/ks.git'
	}
    stage('maven clean') {
	 sh 'mvn clean'
    }
    stage('maven validate') {
	 sh 'mvn validate'
    }
    stage('maven compile') {
     sh 'mvn compile'
    }
    stage('maven test') {
	 sh 'mvn test'
    }
    stage('maven package') {
	 sh 'mvn package'
    }
    stage('maven deployment') {
	 sh 'mvn deploy'
	}
 }
   
     
