def compareGitHash() {
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
}

pipeline {
    agent any

    environment {
        CHANGES = compareGitHash()
    }

    stages {
    when {
        expression {
            return CHANGES == 'true'
        }
    }
        stage ('docker: build') {
            steps {
                script {
                    echo 'works'
                }
            }
        }
    }
}
