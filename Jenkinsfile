pipeline {
	agent any
	stages {
	stage('one') {
	steps {
	echo "Test stage one working"

	}
	}
        stage('git clone') {
            steps {
                sh 'sudo rm -r *;sudo git clone https://github.com/prabus2007/test.git'
            }
           } 
	
	}
}
