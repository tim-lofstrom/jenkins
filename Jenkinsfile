pipeline {
    
    agent any

    stages {
        stage ("scm: check") {
            steps {
                script {
                    def noChanges = ("${GIT_COMMIT}" == "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}")
                    if (noChanges) {
                        currentBuild.result = 'SUCCESS'
                        return
                    }
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
