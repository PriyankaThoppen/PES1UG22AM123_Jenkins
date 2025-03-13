pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh '''
                    g++ -o PES1UG22AM129-1 main.cpp
                    echo "Build completed successfully"
                '''
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh '''
                    ./PES1UG22AM129-1
                    echo "Testing completed successfully"
                '''
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh '''
                    echo "Deployment completed successfully"
                '''
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}
