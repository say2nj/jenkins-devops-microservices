pipeline {

	agent any
	stages{
		stage('Build'){
			steps{
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
