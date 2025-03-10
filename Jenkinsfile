pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'g++ -o hello_exec hello.cpp' // Compiling C++ file
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './non_existent_file' // Running the compiled file
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo Deployment Successful!' // Simulating deployment
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline Failed '
        }
        success {
            echo 'Pipeline Executed Successfully '
        }
    }
}
