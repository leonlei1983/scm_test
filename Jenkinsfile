pipeline {
  agent any

  environment {
    //tag = sh(returnStdout: true, script: "git describe --tags").trim()
    branch = sh(returnStdout: true, script: "git rev-parse --abbrev-ref HEAD").trim()
  }

  stages {
    stage('Build') {
      steps {
        sh 'cat test'
      }
    }

    stage('Git Info') {
      steps {
        //echo tag
        echo branch
        sh 'git branch'
        echo '${env.BRANCH_NAME}'
      }
    }
  }
}
