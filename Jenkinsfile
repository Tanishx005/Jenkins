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
                sh '''
                    sudo apt update
                    sudo apt install -y openjdk-17-jdk
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
