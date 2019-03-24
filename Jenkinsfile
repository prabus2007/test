pipeline {
    agent {
        node {
            label 'master'
        }
    }

    stages {

        stage('terraform started') {
            steps {
                sh 'echo "Started...!" '
            }
        }
        stage('git clone') {
            steps {
                sh 'sudo rm -r *;sudo git clone https://github.com/prabus2007/test.git'
            }
        }
        stage('tfvars create'){
            steps {
                sh 'sudo cp /home/terraform/devops/terraform.tfvars ./jenkins/'
            }
        }
        stage('terraform init') {
            steps {
                sh 'sudo /home/terraform/devops/dev/terraform init ./jenkins'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'ls ./jenkins; sudo /home/terraform/devops/dev/terraform plan ./jenkins'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended....!!"'
            }
        }
        stage('cleaning up the workspace') {
            steps {
                sh 'sudo rm -rf *'
            }
        }
        
    }
}

