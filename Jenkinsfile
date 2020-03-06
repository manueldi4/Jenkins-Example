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
  agent {
    node {
      label 'Development'
    }
  stages {
    stage('Deploy to Dev') {
      steps {
        sh 'cd /home/development'
        sh 'git checkout master'
        sh 'git pull origin master'
        sh 'git checkout dev'
        sh 'git pull origin dev'
        sh 'ls'
      }
    }

  }
}
