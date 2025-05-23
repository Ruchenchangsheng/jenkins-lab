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
                bat '''
                        echo ==== 当前 Python 版本 ====
                        C:\\Users\\chen\\AppData\\Local\\Microsoft\\WindowsApps\\python3.exe --version

                        echo ==== 当前 pip 版本 ====
                        C:\\Users\\chen\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.12_qbz5n2kfra8p0\\LocalCache\\local-packages\\Python312\\Scripts\\pip3.exe --version

                        echo ==== 安装依赖 ====
                        C:\\Users\\chen\\AppData\\Local\\Packages\\PythonSoftwareFoundation.Python.3.12_qbz5n2kfra8p0\\LocalCache\\local-packages\\Python312\\Scripts\\pip3.exe install -r requirements.txt
                        '''
//                 bat 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}
