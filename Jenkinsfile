pipeline {
    agent any

    stages {
        stage('Setup Environment') {
            steps {
                sh '''
                  sudo apt-get update -y
                  sudo apt-get install -y python3 python3-pip
                  pip3 install --break-system-packages pytest
                '''
            }
        }

        stage('Clone Repository') {
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
                sh '''
                  if ls test_*.py > /dev/null 2>&1; then
                      python3 -m pytest
                  else
                      echo "No tests found. Skipping..."
                  fi
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage - placeholder'
            }
        }
    }
}
