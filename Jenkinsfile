pipeline {
    agent {
      node {
        label 'linux && java17'
      }
    }
    stages {
        stage('Hello') {
            steps {
                echo "Hello Pipeline!!! 1"
                echo "Hello Pipeline!!! 2"
                echo "Hello Pipeline!!! 3"
            }
        }
        stage('Build') {
            steps {
                echo "Building the project... 1"
                sleep(10)
                echo "Building the project... 2"
                echo "Building the project... 3"
            }
        }
        stage('Test') {
            steps {
                echo "Testing the project... 1"
                sleep(10)
                echo "Testing the project... 2"
                echo "Testing the project... 3"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the project... 1"
                sleep(10)
                echo "Deploying the project... 2"
                echo "Deploying the project... 3"
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