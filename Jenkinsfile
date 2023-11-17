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

        stage('Copy the Build') {
            steps {
                sh 'docker exec 1f807e2a5e68 ls -l /var/jenkins_home/workspace/Sample-React-App/build'
                sh 'docker cp 1f807e2a5e68:/var/jenkins_home/workspace/Sample-React-App/build /home/nishad-imit/Documents/build'
            }
        }
    }
}