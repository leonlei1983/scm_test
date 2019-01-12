node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'
  def hastag = sh(returnStatus: true, script: 'git describe --tags')
  if (hastag) {
    def tag_name = sh(eturnStdout: true, script: 'git describe --tags').trim()
  }
  echo tag_name
}
