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
                sh 'npm config set http-proxy http://10.252.64.33:8080'
                sh 'npm config set https-proxy http://10.252.64.33:8080'
                sh 'npm install' 
            }
        }
        /* added for tests */
        
        stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */
            steps {
                checkout scm
            }
        }
        stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
            steps {
                app = docker.build("dave-db-app-test")
            }
        }
    }
}
