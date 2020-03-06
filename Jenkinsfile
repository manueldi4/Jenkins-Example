pipeline {
  agent {
    node {
      label 'Test'
    }

  }
  stages {
    stage('Deploy to Test') {
      steps {
        sh 'git checkout master'
      }
    }

  }
}