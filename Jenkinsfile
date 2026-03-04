pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install + Test (venv)') {
            steps {
                sh '''
                    set -e
                    python3 --version

                    # Create and use a virtual environment (avoids PEP 668 system pip restrictions)
                    python3 -m venv .venv
                    . .venv/bin/activate

                    python -m pip install --upgrade pip
                    python -m pip install -e .
                    python -m pip install pytest

                    python -m pytest -v
                '''
            }
        }
    }
}
