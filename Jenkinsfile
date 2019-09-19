pipeline {
    agent {
        docker {
            image 'oavkdtv/centos-node:1.0.0' 
            args '-p 3555:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
