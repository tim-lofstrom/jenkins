def CompareGitHash(){
    return "${GIT_COMMIT}" != "${GIT_PREVIOUS_SUCCESSFUL_COMMIT}";
}

pipeline {
    
    agent any

    environment {
        CHANGES = CompareGitHash()
    }


                    if (!CHANGES) {
                        currentBuild.result = 'SUCCESS'
                        return
                    }

    stages {
        stage ("scm: check") {
            steps {
                script {
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
    }
}
