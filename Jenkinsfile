pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'dev') {
                        echo "Running tests for DEV environment"
                    } else if (env.BRANCH_NAME == 'uat') {
                        echo "Running tests for UAT environment"
                    } else if (env.BRANCH_NAME == 'prod') {
                        echo "Running tests for PROD environment"
                    } else {
                        echo "Branch not recognized, skipping environment-specific steps"
                    }
                }
            }
        }
    }
}
