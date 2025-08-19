pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/Renjithcr20/newproject.git'
            }
        }

        stage('Hello') {
            steps {
                echo 'Hello from Jenkins Pipeline!'
            }
        }
    }
}
