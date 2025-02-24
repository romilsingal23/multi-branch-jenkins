pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
                script {
                    echo "Checked out code from branch: ${env.GIT_BRANCH}"
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    if (env.GIT_BRANCH == 'origin/DEV') {
                        echo "Building for DEV environment"
                    } else if (env.GIT_BRANCH == 'origin/UAT') {
                        echo "Building for UAT environment"
                    } else if (env.GIT_BRANCH == 'origin/PROD') {
                        echo "Building for PROD environment"
                    } else {
                        echo "Branch not recognized, skipping build."
                    }
                }
            }
        }
    }
}
