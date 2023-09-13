pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
			}
		}
               stage('Test') {
                        steps {
                                echo "Build"
                                echo "Test"
                        }
                }
               stage('Integration Test') {
                        steps {
                                echo "Build"
                                echo "Test"
                                echo "Integration Test"
				}
			}
		}
	

	 post {
			always {
				echo "I'm awesome. I run Always"
		}
			success {
				echo "I run when you are successful and for the updated version of my file"
		}
			failure {
				echo "I run when you fail" 
		}
	}
}
