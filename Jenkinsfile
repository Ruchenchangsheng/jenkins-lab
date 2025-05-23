pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Ruchenchangsheng/jenkins-lab.git', branch: 'main'
            }
        }

        stage('Install') {
            steps {
                bat "C:\\Users\\chen\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe -m pip install -r requirements.txt"
            }
        }

        stage('Test') {
            steps {
                bat "C:\\Users\\chen\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe -m pytest"
            }
        }
    }
}
