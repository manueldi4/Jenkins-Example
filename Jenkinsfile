pipeline {
  agent none
  stages {
    stage('Deploy to Test') {
      agent {
        node {
          label 'Test'
        }
      }
      steps {
        sh 'git checkout master'
        sh 'git pull origin master'
        sh 'ls'
      }
    }
    stage('Deploy to Dev') {
      agent {
        node {
          label 'Development'
        }
      }
      steps {
        sh 'git checkout master'
        sh 'git pull origin master'
        sh 'git fetch origin dev'
        sh 'git pull origin dev'
        sh 'ls'
      }
    }
  }
}
