pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('Checkout Code / Git') {
      steps {
        git(url: 'git@github.com:giladifrah/jenkins-ci-template.git', branch: 'master')
      }
    }

  }
}