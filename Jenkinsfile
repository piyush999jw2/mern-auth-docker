
pipeline {
    agent any

    stages {

        stage('System Info') {
            steps {
                sh 'whoami'
                sh 'pwd'
                sh 'node --version'
                sh 'npm --version'
                sh 'ls -la'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing backend dependencies...'
                sh 'npm ci --prefix backend'

                echo 'Installing frontend dependencies...'
                sh 'npm ci --prefix frontend'
            }
        }

        stage('Build Frontend') {
            steps {
                echo 'Building frontend application...'
                sh 'npm run build --prefix frontend'
            }
        }

        stage('Test Backend') {
            steps {
                echo 'Validating backend JavaScript...'
                sh 'node --check backend/server.js'
            }
        }

       

    }
}


