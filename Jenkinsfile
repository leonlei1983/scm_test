node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'
  def hastag = sh(returnStatus: true, returnStdout: false, script: 'git describe --tags')
  if (hastag == 0) {
    def tag_name = sh(returnStdout: true, script: 'git describe --tags').trim()
  }
  if (tag_name) {
    echo tag_name
  }
}
