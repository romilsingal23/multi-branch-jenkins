pipeline {
    agent any
    stages {
        stage('Deploy to Production') {
            when {
                branch 'DEV'
            }
            steps {
                echo 'Deploying to production...'
                // Add deployment steps here
            }
        }
    }
}
