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
                
                sh 'sudo git clone https://github.com/hop101/simple-cicd_pipeline_with_terraform.git'
            }
        }
        stage('terraform init') {
            steps {
                sh 'cd simple-cicd_pipeline_with_terraform; sudo terraform init '
            }
        }
        stage('terraform plan') {
            steps {
                sh 'sudo terraform plan'
            }
        }
        stage('terraform apply') {
            steps {
                sh 'sudo terraform apply'
            }
        }

        
    }
}
