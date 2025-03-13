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
            sh 'mvn deploy'
            echo 'deployment successful'
        }
    }
}

post {
    always {
        script {
            if (currentBuild.result == "FAILURE") {
                echo "Pipeline failed"
            }
        }
    }
}
}
