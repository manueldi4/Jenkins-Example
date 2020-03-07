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
        sh 'git config --global user.email "manuel_diaz@epam.com"
        sh 'git config --global user.name "manueldi4"
        sh 'git pull origin dev'
        sh 'ls'
      }
    }
  }
}
