pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'GitHub repository cloned successfully'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Flask application'
                bat 'pip install flask'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Flask application'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Flask application'
            }
        }
    }
}
