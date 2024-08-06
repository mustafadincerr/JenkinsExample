pipeline {
    agent any

    stages {
        stage('Preparation') {
            steps {
                echo 'Preparing...'
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Building...'
                    sh 'python3 -c "print(\'Hello, Jenkins!\')"'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'python3 -c "assert 1 + 1 == 2"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Deployment completed."'
            }
        }
    }
}
