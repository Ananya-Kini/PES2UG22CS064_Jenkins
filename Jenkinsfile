pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main.cpp -o output'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deployment Successful"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}

