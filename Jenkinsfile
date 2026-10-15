pipeline {
  agent any 
  stages {
    stage("Build") {
    steps {
    sh '''
    apt upade && apt install nginx -y
    sh '''
      stage("Test Services") {
        steps {
        sh '''
        systemctl enable nginx
        systemctl start nginx
        systemctl status nginx
        sh '''
        stage("Deploy") {
          steps {
            sh '''
            http://192.168.200.165:80
            sh '''
    
