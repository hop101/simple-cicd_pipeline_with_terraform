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
                
                sh 'cd /root/jenkins-terraform; sudo rm -r *;sudo git clone https://github.com/hop101/simple-cicd_pipeline_with_terraform.git'
            }
        }
        stage('terraform init') {
            steps {
                sh 'sudo /root/jenkins-terraform/terraform init '
            }
        }
        stage('terraform plan') {
            steps {
                sh 'sudo /root/jenkins-terraform/terraform plan'
            }
        }
        stage('terraform apply') {
            steps {
                sh 'sudo /root/jenkins-terraform/terraform plan'
            }
        }

        
    }
}
