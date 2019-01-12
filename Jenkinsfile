node {
  stage 'Build'
  // docker build
  echo "${env.BRANCH_NAME}"

  stage 'Push'
  // docker push
  sh 'ls -l'
  sh 'printenv'
  def tag_obj = sh(returnStatus: true, returnStdout: true, script: 'git describe --tags')
  echo tag_obj.getStatus()
  echo tag_obj.getStdout()
}
