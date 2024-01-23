pipeline {
	agent any
	stages {
	    stage('Build') { 
		steps {
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
			echo "Integ Test"
		}	
		}		
	} post {
		always {
			echo "the echo always"
			}
		success {
			echo "the echo on success"
			}
		failure {
			echo "the echo on failure"
			}
	}
}
