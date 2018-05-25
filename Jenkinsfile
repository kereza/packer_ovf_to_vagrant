pipeline {
    agent any
    
    environment {
        CC = 'clang'
    }    
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "${env.BUILD_ID}"
                git credentialsId: 'personal_git', url: 'git@github.com:kereza/bash.git'
                git credentialsId: 'personal_git', url: 'git@github.com:kereza/packer_ansible_roles.git'
                sh "mv packer_ansible_roles roles"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
