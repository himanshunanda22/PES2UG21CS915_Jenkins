pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Compile the hello.cpp file
                sh 'g++ -o hello hello.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                // Execute the compiled hello.cpp file
                sh './hello'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps if needed
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
