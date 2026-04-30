// This is the test file for Jenkins.
flag=true

pipeline {
	agent any
	environment {
		// variables here can be used by any stage
		NEW_VERSION = '1.3.0'
	}
	
	stages {
		stage("Build") {
			steps {
			echo "Building.."
			// Here you can define commands for your build
				echo "Building version ${NEW_VERSION}"
			}
		}
		stage("Test") {
			when {
				expression {
					flag == false
				}
			}
			steps {
				echo "Testing.."
			// Here you can define commands for your tests
			}
		}
		stage("Deploy") {
			steps {
			echo "Deploying...."
			// Here you can define commands for your deployment
			}
		}
	}
			post {
			// These conditions wil wxecute after the build is done
			always {
				// This action will happen regardless the output of the build
				echo 'Post build condition running'
			}
			failure {
				// This action will occur only if the build is failed
				echo 'Post action if Build failed'
			}
		}
}
