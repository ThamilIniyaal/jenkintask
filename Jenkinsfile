pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Pulling code from GitHub..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'ls -l'
            }
        }

        stage('Test') {
            steps {
                echo "Testing HTML file..."
                sh 'cat index.html'
            }
        }

        stage('Archive') {
            steps {
                echo "Archiving artifact..."
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }
    }
}
