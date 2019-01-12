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
        gittag = sh(returnStdout: true, script: "git describe --tags || echo").trim()
      }
      steps {
        //sh 'printenv'
        //echo "${gittag}"
        //echo "${env.BRANCH_NAME}"
        sh 'git tag -l'
      }
    }
  }
}
