pipeline {
    agent any

    environment {
        TEST = "development"
        BRANCH_NAME = "${GIT_BRANCH.split("/")[1]}"
    }

    stages {
        stage('Build') {
            steps {
                sh 'printenv'
                sh "echo ${BRANCH_NAME}"
            }
        }
        stage ('test statement') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'development') {
                        echo "This is development branch"
                    }
                }
            }
        }
    }
}
