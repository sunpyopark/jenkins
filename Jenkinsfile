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
            git 'https://github.com/sunpyopark/node-todo-frontend'
        }
        stage('terraform init') {
            steps {
                sh 'sudo /var/lib/jenkins/workspace/terraform-pipeline/terraform init ./jenkins'
            }
        }
        stage('terraform plan') {
            steps {
                sh 'ls ./jenkins; sudo /home/ubuntu/terraform-pipeline/terraform plan ./jenkins'
            }
        }
        stage('terraform ended') {
            steps {
                sh 'echo "Ended....!!"'
            }
        }

        
    }
}
