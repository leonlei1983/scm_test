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
      def tag = sh(returnStdout: true, script: "git describe --tags").trim()
      def branch = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
      steps {
        echo taga
        echo brancha
        echo tag
        echo branch
      }
    }
  }
}
