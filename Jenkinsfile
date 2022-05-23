pipeline {
	agent any
	// agent { docker { image 'node:13.8'} }
	environment{
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps{
				// sh 'sudo usermod -a -G docker jenkins'
				// sh 'node --version'
				sh 'mvn --version'
				sh 'docker --version'
				echo "Hello World- Build"
				echo "Build Number: $env.BUILD_NUMBER"
				echo "Build ID: $env.BUILD_ID"
				echo "Job Name: $env.JOB_NAME"
			}
		}
		
		stage('Test'){
			steps{
				echo "Hello World- Test"
			}
		}
		
		stage('Integration Test'){
			steps{
				echo "Hello World- Integration Test"
			}
		}
	}
	post{
		always{
			echo "Always"
		}
		success{
			echo "Successful"
		}
		failure{
			echo "Failed"
		}
	}

}
