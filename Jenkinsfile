pipeline {
	agent { docker { image 'maven:3.6.3'} }
	stages {
	    stage('Build') { 
		steps {
			sh 'maven --version'
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
