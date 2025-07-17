CODE_CHANGES = getGitChanges()

pipeline {
    agent any
    stages {
        stage('build') {
            when {
                    expression { 
                      BRANCH_NAME == 'main' && CODE_CHANGES = true
                    }
            }
            steps {
                echo 'Building the application...'
                // your build commands
            }
        }
        stage('Test') {
            when {
                    expression { BRANCH_NAME == 'development' }
            }
            steps {
                echo 'Running tests...'
                // your test commands
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // your deploy commands
            }
        }
    }
}
