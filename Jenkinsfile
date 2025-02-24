pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                script {
                    if (env.GIT_BRANCH == 'master') {
                        echo 'Deploying to production...'
                        // Add production deployment steps
                    } else if (env.GIT_BRANCH == 'dev') {
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
