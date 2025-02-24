pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                script {
                    checkout scm
                }
                echo "checked out branch: ${env.GIT_BRANCH}"
                echo "checked out branch: ${env.BRANCH_NAME}"
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                    if (env.GIT_BRANCH == 'master') {
                        echo 'Deploying to production...'
                        // Add production deployment steps
                    } else if (env.GIT_BRANCH == 'origin/DEV') {
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
