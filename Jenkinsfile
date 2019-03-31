pipeline {
	agent any
	stages {
	stage('one') {
	steps {
	echo "Test stage one working"

	}
	}
	stage('two') {
	steps {
	input('Do you want to proceed ?')
	}
	}
	
	}
}
