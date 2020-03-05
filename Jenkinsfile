pipeline {
  agent {
    node {
      label 'unreal'
    }

  }
  stages {
    stage('build') {
      agent {
        node {
          label 'unreal'
        }

      }
      steps {
        git(url: 'https://github.com/Tenbatsu589/guerilla-games', branch: 'master', changelog: true)
        bat(script: 'build.bat', returnStatus: true, returnStdout: true)
      }
    }

  }
}