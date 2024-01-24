pipeline {
	//agent { docker { image 'node:16.20'} }
	agent any
	environment {
		dockerHome = tool 'MyDocker'
		mavenHome = tool 'MyMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
	    stage('Build') { 
		steps {
			sh 'mvn --version'
			sh 'docker version'
			echo "Build"
		}	
		}
	    stage('test') { 
		steps {
			echo "test"
		}	
		}
	    stage('Integration Test') { 
		steps {
			echo "Integrationnnnnn Test"
		}	
		}		
	} 
	post {
		always {
			echo 'the echo always'
			}
		success {
			echo 'the echo on success'
			}
		failure {
			echo 'the echo on failure'
			}
	}
}
