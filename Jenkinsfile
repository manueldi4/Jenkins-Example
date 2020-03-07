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
        sh 'cd /home/test/Jenkins-Example'
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
        sh 'cd /home/development/Jenkins-Example'
        sh 'git checkout master'
        sh 'git pull origin master'
        sh 'git checkout dev'
        sh 'git pull origin dev'
        sh 'ls'
      }
    }
  }
}
