pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/example/repo.git'
            }
        }
        stage('Copy Files') {
            steps {
                sh 'scp -r path/to/files user@remote:/path/to/destination'
            }
        }
    }
    post {
        success {
            emailext body: 'Your Jenkins job has completed successfully',
                     subject: 'Jenkins Job Successful',
                     to: 'your-email@example.com'
        }
    }
}
