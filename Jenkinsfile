pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/msshabreena-coder/jenkins-project1.git'
            }
        }

        stage('CompileCheck') {
            steps {
                bat 'python -m py_compile app.py'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded: app.py has no syntax errors.'
        }

        failure {
            echo 'Build failed: check app.py for syntax errors.'
        }
    }
}
