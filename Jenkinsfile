pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
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
