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
                echo "exiting with code 0"
                exit 0
            }
        }
        stage ('third_stage') {
            steps {
                echo "reachable?"
            }
        }
    }
}