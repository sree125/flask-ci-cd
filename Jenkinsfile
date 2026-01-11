pipeline {
    agent any

    stages {
        stage('Install pip & dependencies') {
            steps {
                sh '''
                    sudo apt update
                    sudo apt install -y python3-pip
                    pip3 install --user flask
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
