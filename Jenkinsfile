def compareGitHash() {
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
}

pipeline {
    agent any

    environment {
        CHANGES = compareGitHash()
    }

    expression {
        return env.shouldBuild = CHANGES
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
