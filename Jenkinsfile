pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/msshabreena-coder/jenkins-project1.git'
            }
        }

        stage('Show BuildInfo') {
            steps {
                echo "Build Number: ${env.BUILD_NUMBER}"
                echo "Job Name: ${env.JOB_NAME}"
                echo "Workspace: ${env.WORKSPACE}"
            }
        }

        stage('RunLinter') {
            steps {
                bat 'flake8 app.py'
            }
        }
    }
}
