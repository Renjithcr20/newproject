pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Renjithcr20/newproject.git',
                    
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'mvn clean install'   // for Java (Maven)
                // sh './gradlew build'  // for Java (Gradle)
                // sh 'npm install'      // for Node.js
                // sh 'python setup.py build' // for Python
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'   // Java Maven
                // sh 'npm test'   // Node.js
                // sh 'pytest'     // Python
            }
        }
    }
}
