pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Tanishx005/Jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                bat 'python -m unittest test_app.py'
            }
        }

        stage('Build') {
            steps {
                echo 'Flask application built successfully!'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                    if exist C:\\flask-deployment rmdir /S /Q C:\\flask-deployment
                    mkdir C:\\flask-deployment

                    xcopy /E /I /Y app.py C:\\flask-deployment
                    xcopy /E /I /Y requirements.txt C:\\flask-deployment
                    xcopy /E /I /Y templates C:\\flask-deployment\\templates
                '''
            }
        }
    }
}
