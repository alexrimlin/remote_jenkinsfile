pipeline {
    agent any
    stages {
        stage ('first_stage') {
            steps {
                echo "executing echo 1"
            }
        }
        stage ('another_stage') {
            steps {
                echo "reachable?"
            }
        }
        stage ('failed_stage') {
            steps {
                exit 0
            }
        }
    }
}