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
      environment {
        tag_name = sh(returnStdout: true, script: "git describe --tags")
      }
      steps {
        echo "${tag_name}"
        echo "${env.BRANCH_NAME}"
        sh 'git tag -l'
        sh 'printenv'
      }
    }
  }
}
