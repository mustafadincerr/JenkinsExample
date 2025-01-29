pipeline {
    agent any

    stages {
        stage('Preparation') {
            steps {
                echo 'Preparing...'
                
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    echo 'Building Docker Image...'
                    sh 'docker build -t my-jenkins:latest .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    echo 'Running Docker Container...'
                    sh 'docker run -d -p 8081:8080 -p 50001:50000 --name my-jenkins-container my-jenkins:latest'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                   
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying...'
                    
                }
            }
        }
    }

    post {
        always {
            script {
                echo 'Cleaning up...'
                sh 'docker stop my-jenkins-container || true'
                sh 'docker rm my-jenkins-container || true'
            }
        }
    }
}

