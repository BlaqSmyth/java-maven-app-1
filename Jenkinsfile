pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description:'')
        booleanParam(name: 'executeTests', defaultValue: true, decription:'')
    }
    stages {
        stage("build") {
            steps {
                // Build steps go here
                echo 'building the application...'
            }
        }
        stage("test") {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                // Test steps go here
                echo 'testing the applications...'
            }
        }
        stage("deploy") {
            steps {
                // Deploy steps go here
                echo 'deploying the applications...'
                echo "deploying version ${params.VERSION}"
            }
        }
    }
}
