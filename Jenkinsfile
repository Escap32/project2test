pipeline {
	agent any
	// agent { docker { image 'node:13.8'} }

	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH" 
	}
	stages {
		stage('Build') {
			steps {
				sh 'docker version'
				sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                                echo "BUILD_ID - $env.BUILD_ID"
                                echo "JOB_NAME - $env.JOB_NAME"
                                echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
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
			changed {
				echo "just to see"
		}
	}
}
