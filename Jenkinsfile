pipeline {
  agent any 
  stages {
    stage("Build") {
    steps {
    sh '''
    sudo apt update && sudo apt install nginx -y
        sh '''
    }
    }
      stage("Test Services") {
        steps {
        sh '''
        sudo systemctl enable nginx
        sudo systemctl start nginx
        sudo systemctl status nginx
        sh '''
        }
      }
        stage("Deploy") {
          steps {
            sh '''
            http://192.168.200.165:80
            sh '''
          }
        }
  }
}
