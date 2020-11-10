node {
    printMessage("Pipeline Start..")

    stage("Fetch Source Code") {
        sh "echo stuff"
    }

    dir('./') {
        stage("Install Requirements") {
            sh 'echo install'
        }

        stage("Run Tests") {
            sh 'echo jenkins_test'
        }

        stage("Deploy") {
            if (env.BRANCH_NAME == "master") {
                printMessage("deploying master branch")
            } else {
                printMessage("no deployment specified for this branch")
            }
        }
    }

    printMessage("Pipeline End")
}

def printMessage(message) {
    echo "${message}"
}
