pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                sh '''
                    python3 -m pip install --user flask
                '''
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
            echo 'Flask app ran successfully 🎉'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}
