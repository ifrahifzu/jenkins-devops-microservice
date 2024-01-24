pipeline {
	//agent { docker { image 'node:16.20'} }
	agent { docker { image 'maven:3.9.6'} }
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
	    stage('checkout') { 
		steps {
			sh 'mvn --version'


			echo "Build"
			echo "path --> $PATH"

			echo "docker path --> $env.dockerHome"
			echo "maven path --> $env.mavenHome"			
            echo "build_number --> $env.BUILD_NUMBER"
            echo "build_id --> $env.BUILD_ID"
            echo "build_number --> $env.JOB_NAME"
            echo "build_number --> $env.BUILD_TAG"
            echo "build_number --> $env.BUILD_URL"
		}	
		}
		stage ('Compile') {
			steps {
				sh "mvn clean compile"
			}
		}
	    stage('test') { 
		steps {
			sh "mvn test"
		}	
		}
	    stage('Integration Test') { 
		steps {
			echo "mvn failsafe:integration-test failsafe:verify"
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
