node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'
  def hastag = sh(returnStatus: true, returnStdout: false, script: 'git describe --tags')
  echo hastag
  if (hastag) {
    def tag_name = sh(returnStdout: true, script: 'git describe --tags').trim()
  }
  echo tag_name
}
