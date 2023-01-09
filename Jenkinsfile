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
      }
    }

    stage('Build') {
      steps {
        bat '''cd src\\MyWindowsService
        nuget restore -source "https://api.nuget.org/v3/index.json"'''
      }
    }

    stage('Build / msbuild') {
      steps {
        bat 'msbuild src\\\\MyWindowsService\\\\MyWIndowsService\\\\Deploy-Windows-Service-Via-MSBuild.proj'
      }
    }

  }
}
