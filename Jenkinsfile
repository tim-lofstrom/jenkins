def compareGitHash() {
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
}

pipeline {
    agent any

    environment {
        CHANGES = compareGitHash()
    }

    stages {
        stage ('docker: build') {
            when {
                environment name: 'CHANGES', value: true
            }
            steps {
                script {
                    echo 'works'
                }
            }
        }
    }
}
