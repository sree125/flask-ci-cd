pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/sree125/flask-ci-cd.git'
            }
        }

        stage('Check Python Version') {
            steps {
                sh 'python3 --version'
            }
        }

        stage('Run Python Script') {
            steps {
                sh 'python3 app.py'
            }
        }
    }

    post {
        success {
            echo 'Python script executed successfully 🎉'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}
