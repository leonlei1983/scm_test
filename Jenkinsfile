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
        tag_obj = sh(returnStatus: true, returnStdout: true, returnStderr: true, script: "git describe --tags")
        tag_name = tag_obj.getStdout()
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
