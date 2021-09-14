def commitHashForBuild(build) {
  def scmAction = build?.actions.find { action -> action instanceof jenkins.scm.api.SCMRevisionAction }
  return scmAction?.revision?.hash
}

def getLastSuccessfulCommit() {
  def lastSuccessfulHash = null
  def lastSuccessfulBuild = currentBuild.rawBuild.getPreviousSuccessfulBuild()
  if ( lastSuccessfulBuild ) {
    lastSuccessfulHash = commitHashForBuild(lastSuccessfulBuild)
  }
  return lastSuccessfulHash
}

pipeline {
    
    agent any

    stages {
        stage ("scm: check") {
            steps {
                script {
                    def lastSuccessfulCommit = getLastSuccessfulCommit()
                    echo "${lastSuccessfulCommit}"
                    echo "${GIT_COMMIT}"
                }
            }
        }

        stage ("docker: build") {
            steps {
                script {
                    echo "works"
                }
            }
        }

        stage ("docker: push registry") {
            steps {
                script {
                    echo "works"
                }
            }
        }

        stage ("openshift: deploy") {
            steps {
                script {
                    echo "works"
                }
            }
        }

    }
}
