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
                echo "Listing files..."
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo "Displaying HTML file..."
                bat 'type index.html'
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
