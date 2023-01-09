pipeline {
  agent {
    node {
      label 'windows'
    }

  }
  stages {
    stage('Check Out') {
      steps {
        git(url: 'git@github.com:giladifrah/jenkins-ci-template.git', branch: 'master', poll: true, credentialsId: 'giladgit-ssh')
        build 'bat \'\'\'cd src\\\\MyWindowsService           nuget restore -source "https://api.nuget.org/v3/index.json"\'\'\''
      }
    }

  }
}