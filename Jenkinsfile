pipeline {
    agent any

    stages {
        stage("Set Variables") {
            steps {
                script {
                    if ("${env.BRANCH_NAME}" == "master") {
                        echo "Now you're ${BRANCH_NAME}"
                    }
                    else if ("${env.BRANCH_NAME}" == "testing") {
                        echo "Now you're ${BRANCH_NAME}"
                    }
                    else if ("${env.BRANCH_NAME}" == "release") {
                        echo "Now you're ${BRANCH_NAME}"
                    }
                    else {
                        echo "Now you're ${BRANCH_NAME}"
                    }
                }
            }
        }
    }
    post {
        always {
            echo "Release finished do cleanup"
            deleteDir()
        }
        success {
            echo "Release Success"
        }
        failure {
            echo "Release Failed"
        }
        cleanup {
            echo "Clean up in post work space"
            cleanWs()
        }
    }
}
