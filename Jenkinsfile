def compareGitHash() {
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}"
}

pipeline {
    agent any

    environment {
        CHANGES = compareGitHash()
    }

    parameters {
        booleanParam(defaultValue: true, description: 'Execute pipeline?', name: 'shouldBuild')
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
