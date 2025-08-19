
      pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Renjithcr20/newproject.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                // 👇 Change this based on your project
               

                              

                // For Python:
                // sh 'python setup.py build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
               

            
                // For Python:
                // sh 'pytest'
            }
        }

        stage('Hello') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
            }
        }
    }
}
