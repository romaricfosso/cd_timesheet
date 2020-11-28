node {
def app
def registryProjet="romaricfosso/cd_timesheet"
def IMAGE_NAME = "${registryProject}:cd_timesheet-${env.BUILD_ID}"
  stage ('Clone from git')
{
  sh 'rm -rf *'
  git "https://github.com/romaricfosso/cd_timesheet.git"
}
}
