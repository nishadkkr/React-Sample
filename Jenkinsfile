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
    }
    post {
        always {
            docker.image('myjenkins-blueocean:1.0.1').inside {
            sh 'cp -r /var/jenkins_home/workspace/Sample-React-App/build /home/nishad-imit/Documents/Build'
                }
            }
        }
}