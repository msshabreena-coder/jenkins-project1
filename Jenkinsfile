pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/msshabreena-coder/jenkins-project1.git'
            }
        }

        stage('InstallDependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('RunUnitTests') {
            steps {
                bat 'pytest test_app.py'
            }
        }
    }
}
