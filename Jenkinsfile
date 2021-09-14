pipeline {
    
    agent any

    environment {
        CHANGES = ("${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}")
    }

    if (!CHANGES) {
        currentBuild.result = 'SUCCESS'
        return
    }

    stages {

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
