pipeline {
  agent any

  //environment {
    //tag = sh(returnStdout: true, script: "git describe --tags").trim()
  //}

  stages {
    stage('Build') {
      steps {
        sh 'cat test'
      }
    }

    stage('Git Info') {
      steps {
        echo "${env.BRANCH_NAME}"
        sh 'printenv'
        tag = sh(returnStdout: true, script: "git describe --tags").trim()
        echo "${tag}"
      }
    }
  }
}
