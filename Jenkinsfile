pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Tanishx005/Jenkins.git'
            }
        }

        stage('Install Java') {
            steps {
                bat '''
                    java -version
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed successfully!'
            }
        }
    }
}
