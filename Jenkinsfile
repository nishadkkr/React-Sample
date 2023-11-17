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

    post {
        always {
            script {
                docker.image('fe98fc51eb70').inside('-v /home/nishad-imit/Documents/Build:/var/jenkins_home/workspace/Sample-React-App') {
                sh 'cp -r /var/jenkins_home/workspace/Sample-React-App/build /home/nishad-imit/Documents/Build'
                    }
                }
            }
        }
    }
}