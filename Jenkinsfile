def compareGitHash() {
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
}

pipeline {
    agent any

    environment {
        CHANGES = compareGitHash()
    }

    when {
                expression {
                    return CHANGES == 'true'
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
