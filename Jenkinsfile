pipeline {
    agent {
        docker {
            image 'oavkdtv/centos-node:1.0.0' 
            args '-p 3555:3000' 
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm config set http-proxy http://10.252.64.33:8080'
                sh 'npm config set https-proxy http://10.252.64.33:8080'
                sh 'npm install' 
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}
