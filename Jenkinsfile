pipeline {

	agent { docker { image 'maven:3.6.3'} }
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				echo "Hello World- Build"
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
