pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script{
                    // Build steps go here
                    echo "Testing the application..."
                    echo "Executing pipeline for branch $BRANCH_NAME"
                } 
            }
        }
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == "master"
                }
            }
            steps {
                script{
                    // Test steps go here
                    "echo 'Building the applications..."
                }
            }
        }
        stage("deploy") {
            when {
                expression {
                    BRANCH_NAME == "master"
                }
            }
            steps {
                script{
                    // Test steps go here
                    echo "Deploying the applications..."
                }
            }
        }
    }
}
