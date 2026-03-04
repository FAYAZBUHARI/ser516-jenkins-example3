pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install') {
            steps {
                sh '''
                    python3 --version || python --version
                    python3 -m pip install --upgrade pip || python -m pip install --upgrade pip
                    python3 -m pip install -e . pytest || python -m pip install -e . pytest
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                    python3 -m pytest -v || python -m pytest -v
                '''
            }
        }
    }
}
