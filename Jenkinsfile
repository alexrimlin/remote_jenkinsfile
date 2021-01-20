pipeline {
    agent any
    stages {
        stage ('first_stage') {
            steps {
                echo "executing echo 1"
            }
        }
        stage ('second_stage') {
            steps {
                echo "exiting 2 with an error code"
                exit 3
            }
        }
        stage ('third_stage') {
            steps {
                echo "probably unreachable stage"
            }
        }
    }
}