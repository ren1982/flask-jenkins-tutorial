pipeline {
  agent { docker { image 'python:3.8.1' } }
  stages {
    stage('build') {
      steps {
        sh 'pip install --user -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }
    }
  }
}