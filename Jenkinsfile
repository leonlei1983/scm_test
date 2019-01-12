node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'

  def tag_name = 'latest'
  if (hastag == 0) {
    tag_name = sh(returnStdout: true, script: 'git describe --tags').trim()
  }
  echo tag_name
}
