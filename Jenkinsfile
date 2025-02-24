pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
        
            }
        }

        stage('Build for DEV') {
            when { branch 'dev' }
            steps {
                echo "Building for DEV environment"
            }
        }

        stage('Build for UAT') {
            when { branch 'uat' }
            steps {
                echo "Building for UAT environment"
            }
        }

        stage('Build for PROD') {
            when { branch 'prod' }
            steps {
                echo "Building for PROD environment"
            }
        }
    }
}
