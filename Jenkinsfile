pipeline {
  agent {
    node {
      label 'Test'
    }

  }
  stages {
    stage('Deploy to Test') {
      steps {
        sh 'cd /home/test'
        sh 'git checkout master'
        sh 'git pull origin master'
        sh 'ls'
      }
    }

  }
}
