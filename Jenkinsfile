pipeline {
  agent any

  environment {
    taga = sh(returnStdout: true, script: "git describe --tags").trim()
    brancha = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
  }

  stages {
    stage('Build') {
      steps {
        sh 'cat test'
      }
    }

    stage('Build') {
      steps {
        echo taga
        echo brancha
        echo tag
        echo branch
      }
    }
  }
}
