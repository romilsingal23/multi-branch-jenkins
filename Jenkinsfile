pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'main') {
                        echo 'Deploying to production...'
                        // Add production deployment steps
                    } else if (env.BRANCH_NAME == 'dev') {
                        echo 'Deploying to staging...'
                        // Add staging deployment steps
                    } else {
                        echo 'Skipping deployment for feature branch'
                    }
                }
            }
        }
    }
}
