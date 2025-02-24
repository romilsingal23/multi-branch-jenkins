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

        stage('Build for DEV') {
            when {
                expression { return env.GIT_BRANCH == 'origin/DEV' }
            }
            steps {
                echo "Building for DEV environment"
            }
        }

        stage('Build for UAT') {
            when {
                expression { return env.GIT_BRANCH == 'origin/UAT' }
            }
            steps {
                echo "Building for UAT environment"
            }
        }

        stage('Build for PROD') {
            when {
                expression { return env.GIT_BRANCH == 'origin/PROD' }
            }
            steps {
                echo "Building for PROD environment"
            }
        }
    }
}
