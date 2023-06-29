pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                script {
                    def nodejsTool = tool name: 'node-20-tool', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
                    env.PATH = "${nodejsTool}/bin:${env.PATH}"
                }
                
                sh 'node --version'
                echo 'Running tests...'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }
        
        stage('Docker') {
            steps {
                script {
                    def dockerTool = tool name: 'docker-latest-tool', type: 'org.jenkinsci.plugins.docker.commons.tools.DockerTool'
                    env.PATH = "${dockerTool}/bin:${env.PATH}"
                }
                
                sh 'docker --version'
                echo 'Building image and pushing to Docker Hub...'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application to EC2 instance...'
            }
        }
    }
}
