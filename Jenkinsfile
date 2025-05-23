pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Ruchenchangsheng/jenkins-lab.git', branch: 'main'
            }
        }
        stage('Debug') {
            steps {
                bat 'where python'
                bat 'python --version'
                bat 'pip --version'
            }
        }
        stage('Install') {
            steps {
                bat 'C:/Users/chen/AppData/Local/Microsoft/WindowsApps/python.exe pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}
