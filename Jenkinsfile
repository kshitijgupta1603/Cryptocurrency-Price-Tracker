pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/kshitijgupta1603/Cryptocurrency-Price-Tracker.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build App') {
            steps {
                sh 'npm run build'
            }
        }
    }

    post {
        success {
            echo 'Build successful. Files are in the dist/ directory.'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
