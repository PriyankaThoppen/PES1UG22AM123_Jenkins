pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o PES1UG22AM123-1 hello.cpp'
        }
    }
    
    stage('Test') {
        steps {
            sh './PES1UG22AM123-1'
        }
    }
    
    stage('Deploy') {
        steps {
            // deployment code
            echo 'Deploying the application..'
            sh '''
                echo "Deployment completed succesfully
            '''
        }
    }
}

post {
    failure {
        echo 'Pipeline failed!'
    }
    success {
        echo 'Pipeline completed successfully'
    }
}
}
