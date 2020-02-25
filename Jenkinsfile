pipeline {
  agent { docker { image 'python:3.8.1' } }
  stages {
    stage('build') {
      steps {
        sh 'python -m venv myenv'
        sh 'source myenv/bin/activate'
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }
    }
  }
}