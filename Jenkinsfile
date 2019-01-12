node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'

  def tag_name = 'latest'
  try {
    tag_name = sh(returnStdout: true, script: 'git describe --tags').trim()
  } catch(err) {
    //
  }
  echo tag_name
}
