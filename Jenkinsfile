
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    set -e
                    sudo -n apt-get update
                    sudo -n apt-get install -y nginx
                '''
            }
        }

        stage('Test Services') {
            steps {
                sh '''
                    set -e
                    sudo -n systemctl enable nginx
                    sudo -n systemctl start nginx
                    sudo -n systemctl is-active nginx
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    set -e
                    curl -fI http://127.0.0.1:80
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
