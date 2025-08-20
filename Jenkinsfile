
   pipeline {
    agent any

    stages {
        stage('Setup Python') {
            steps {
                sh '''
                  sudo apt-get update -y
                  sudo apt-get install -y python3 python3-pip
                  pip3 install --break-system-packages pytest
                '''
            }
        }

        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Renjithcr20/newproject.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'python3 hello.py build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest'
            }
        }
    }
}
