pipeline {
    agent any
    stages {
        stage('Pull Files') {
            steps {
                sh 'ssh ubuntu@13.232.66.159 "git clone https://github.com/shashank-1-1/git-jenkin-test.git /home/ubuntu"'
            }
        }
    }
    post {
        success {
            emailext body: 'Jenkins job has completed successfully',
                     subject: 'Jenkins Job Successful',
                     to: 'shashank.shekhar.jg@hitachi-systems.com'
        }
    }
}
