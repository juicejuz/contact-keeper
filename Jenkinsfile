pipeline {
  agent {
    node {
      label 'node'
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