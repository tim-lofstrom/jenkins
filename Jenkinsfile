def compareGitHash() {
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
}

pipeline {
    agent any

    environment {
        CHANGES = compareGitHash()
    }

    stages {
        stage ('scm: check') {
            script {
                if (!CHANGES) {
                    currentBuild.result = 'SUCCESS'
                    return
                }
            }

            stages {
                stage ('docker: build') {
                    steps {
                        script {
                            echo 'works'
                        }
                    }
                }
            }
        }
    }
}
