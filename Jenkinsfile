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
                
                sh 'rm -rf *; git clone https://github.com/hop101/simple-cicd_pipeline_with_terraform.git'
            }
        }
        stage('terraform init') {
            steps {
                sh 'cd simple-cicd_pipeline_with_terraform; terraform init '
            }
        }
        stage('terraform plan') {
            steps {
                sh 'cd simple-cicd_pipeline_with_terraform; terraform plan'
            }
        }
        stage('terraform apply') {
            steps {
                sh 'cd simple-cicd_pipeline_with_terraform; terraform apply --auto-approve'
            }
        }

        
    }
}
