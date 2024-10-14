pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'make' // or any build command you need
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'make test' // run your tests
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'make deploy' // your deployment command
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
