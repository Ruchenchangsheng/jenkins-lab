pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                bat 'dir'
                git url: 'https://github.com/Ruchenchangsheng/jenkins-lab.git', branch: 'main'
            }
        }
        stage('Verify Python') {
            steps {
                bat 'python --version'
                bat 'pip --version'
            }
        }
        stage('Install') {
            steps {
                bat '''
                echo Installing Python dependencies...
                pip install -r requirements.txt
                if %errorlevel% neq 0 exit /b %errorlevel%
                '''
//                 bat 'pip install -r requirements.txt '
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}
