node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'
  def hastag = sh(returnStatus: true, returnStdout: false, script: 'git describe --tags')

  def tag_name = NULL
  if (hastag == 0) {
    tag_name = sh(returnStdout: true, script: 'git describe --tags').trim()
  }
  try {
    echo tag_name
  } catch (err) {
    //
  }
}
