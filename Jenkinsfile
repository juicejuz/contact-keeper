pipeline {
    agent {
        docker {
            image 'oavkdtv/centos-node' 
            args '-p 3000:3000' 
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
