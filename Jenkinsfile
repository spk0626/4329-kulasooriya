pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the repository
                git branch: 'master', url: 'https://github.com/monilkarajapaksha/NodeBackend'
            }
        }
        stage('Dockerize the Application') {
            steps {
                // Build Docker image
                script {
                    docker.build('node-app')
                }
            }
        }
        stage('Run Container') {
            steps {
                // Run Docker container
                script {
                    docker.image('node-app').run('-p 3000:3000')
                }
            }
        }
    }
}

//git branch: 'main', url: 'https://github.com/spk0626/4329-kulasooriya.git'