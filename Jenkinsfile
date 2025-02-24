pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
                echo "Checked out code from branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Build for DEV') {
            when { expression { env.BRANCH_NAME.endsWith('/dev') || env.BRANCH_NAME == 'dev' } }
            steps {
                echo "Building for DEV environment"
            }
        }

        stage('Build for UAT') {
            when { expression { env.BRANCH_NAME.endsWith('/uat') || env.BRANCH_NAME == 'uat' } }
            steps {
                echo "Building for UAT environment"
            }
        }

        stage('Build for PROD') {
            when { expression { env.BRANCH_NAME.endsWith('/prod') || env.BRANCH_NAME == 'prod' } }
            steps {
                echo "Building for PROD environment"
            }
        }
    }
}
