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
                sh 'sudo git clone https://github.com/sunpyopark/jenkins.git'
            }
        }
        stage('terraform init') {
            steps {
                sh 'sudo /var/lib/jenkins/workspace/terraform-pipeline/terraform init'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'sudo /var/lib/jenkins/workspace/terraform-pipeline/terraform plan'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended....!!"'
            }
        }

        
    }
}
