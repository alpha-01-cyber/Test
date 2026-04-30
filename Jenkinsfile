// This is the test file for Jenkins.
pipeline {
	agent any
	stages {
		stage("Build") {
			steps {
			echo "Building.."
			// Here you can define commands for your build
			}
		}
		stage("Test") {
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
			faliure {
				// This action will occur only if the build is failed
				echo 'Post action if Build failed'
			}
		}
}
