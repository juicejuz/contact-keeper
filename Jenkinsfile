pipeline {
  agent {
    node {
      label 'test-ci'
    }

  }
  stages {
    stage('test-1') {
      steps {
        git(url: 'https://github.com/juicejuz/contact-keeper', branch: 'master', changelog: true)
      }
    }
    stage('test-2') {
      steps {
        sh '''npm install
node app.js'''
      }
    }
  }
}