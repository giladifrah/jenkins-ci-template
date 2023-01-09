pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('Check Out') {
      steps {
        git(url: 'git@github.com:giladifrah/jenkins-ci-template.git', branch: 'master', poll: true)
      }
    }

  }
}