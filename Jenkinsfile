
pipeline {
    agent any

    stages 
    {
        stage('Start') {
            steps {
                sh 'ls'
            }
        }

        stage ('load script') {
            steps {
                def code = load 'test_job.groovy'
            }
        }
        stage('Groovy') {
            steps {
                code.foo()
            }
        }
        stage('End') {
            steps {
                sh 'ls'
            }
        }
    }
}
