pipeline {
    agent any
    stages {
        stage('Install Dependencies') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Build the Code') {
            steps {
                sh 'npm run build'
            }
        }
    }
}