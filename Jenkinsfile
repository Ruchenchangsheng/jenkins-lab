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
                        python --version
                        echo ==== 当前 pip 版本 ====
                        pip --version
                        echo ==== 安装依赖 ====
                        pip install -r requirements.txt
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
