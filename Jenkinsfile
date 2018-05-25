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
                git credentialsId: 'personal_git', url: 'git@github.com:kereza/packer_ansible_roles.git'
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
