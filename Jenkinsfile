pipeline {
    agent {
      node {
        label 'linux && java17'
      }
    }
    stages {
        stage('Hello') {
            steps {
                echo "Hello Pipeline!!!"
            }
        }
        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }
        stage('Test') {
            steps {
                echo "Testing the project..."
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the project..."
            }
        }
    }
    post {
        always {
            echo "This will always run"
        }
        success {
            echo "This will run only if successful"
        }
        failure {
            echo "This will run only if failed"
        }
        unstable {
            echo "This will run only if the run was marked as unstable"
        }
        changed {
            echo "This will run only if the state of the Pipeline has changed"
            echo "For example, if the Pipeline was previously failing but is now successful"
        }
        cleanup {
            echo "This will always run, doesn't matter if the Pipeline failed or succeeded"
        }
    }
}