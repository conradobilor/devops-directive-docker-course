pipeline {
    agent any

    environment {
        // Define environment variables
        //MY_ENV_VAR = 'some_value'
    }

    stages {
        stage('Checkout') {
            steps {
                //checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                //sh 'scp target/*.jar user@server:/path/to/deploy'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
