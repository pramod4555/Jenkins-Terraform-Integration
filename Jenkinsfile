pipeline {
    agent any
    tools {
        terraform 'Infra'
    }
    stages {
            stage('Git checkout'){
            steps{
            git branch: 'main', credentialsId: 'first', url: 'https://github.com/pramod4555/Terraform.git'
            }
            }
            stage("terraform credentials in environment variables"){
            environment {
            Path ="/usr/local/bin"
            }
            }
            stage('terraform init'){
        steps{
        sh 'terraform init'
        }
        }
        stage('terraform plan'){
        steps{
        sh 'terraform plan'
        }
        }
        stage('terraform apply'){
        steps{
        sh 'terraform apply --auto-approve'
        }
        }
}
 }
