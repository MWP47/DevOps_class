pipeline {
    agent any

    stages {
        stage('Setup Python Environment') {
            steps {
                bat '''
                "C:\\Users\\Lenovo\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" --version
                "C:\\Users\\Lenovo\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" -m venv venv
                call venv\\Scripts\\activate
                python -m pip install --upgrade pip
                pip install -r requirements.txt
                '''
            }
        }

        stage('Run Tests') {
            steps {
                bat '''
                call venv\\Scripts\\activate
                pytest
                '''
            }
        }
    }
}
