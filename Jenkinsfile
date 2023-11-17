pipeline {
    agent any

    tools {
        nodejs "Node"
    }

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

        stage('Copy the build File') {
            steps {
                sh 'cp -r * /home/nishad-imit/Documents/Build'
            }
        }
    }
}