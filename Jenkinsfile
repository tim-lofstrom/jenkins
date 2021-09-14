pipeline {
    
    agent any

    stages {
        stage ("scm: check") {
            steps {
                script {
                    echo "${currentBuild.previousSuccessfulBuild.branch}"
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
