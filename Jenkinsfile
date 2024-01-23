pipeline {
	agent { docker { image 'node:16.20'} }
	stages {
	    stage('Build') { 
		steps {
			sh 'node --version'
			sh  'uname -a'
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
