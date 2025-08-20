pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', url: 'https://github.com/Renjithcr20/newproject.git'
            }
        }

        stage('Setup Python') {
            steps {
                echo 'Setting up Python environment...'
                sh '''
                  sudo apt-get update -y
                  sudo apt-get install -y python3 python3-pip
                  pip3 install --break-system-packages pytest
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                // Example: replace with actual build command
                sh 'python3 hello.py build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'python3 -m pytest'
            }
        }
    }
}
