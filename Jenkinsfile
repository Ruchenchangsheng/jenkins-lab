pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url:'https://github.com/Ruchenchangsheng/jenkins-lab.git', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                bat 'echo 当前路径为：%CD%'
                bat 'dir'
                bat 'where python'
                bat 'where pip'
                bat '"C:\\Users\\chen\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat '"C:\\Users\\chen\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m pytest'
            }
        }
    }
}
