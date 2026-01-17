pipeline {
  agent any

  stages {
    stage("build") {
      steps {
        echo "Testing the application..."
        echo "Executing pipeline for branch ${env.BRANCH_NAME}"
      }
    }
    stage("test") {
      steps {
        echo 'testing the application'
      }
    }
    stage("deploy") {
      steps {
        echo 'deploying the application'
      }
    }
  }
}

