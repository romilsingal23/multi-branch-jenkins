pipeline {
    agent any
    stages {
        stage('Deploy to Production') {
            when {
                branch 'origin/DEV'
            }
            steps {
                echo 'Deploying to production...'
                // Add deployment steps here
            }
        }
    }
}
