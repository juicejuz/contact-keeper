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
    stage('docker') {
      steps {
        sh 'docker build -t dave-test --target prod .'
      }
    }
  }
}