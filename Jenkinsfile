
// pipeline {
//     agent any

//     stages 
//     {
//         stage('Start') {
//             steps {
//                 sh 'ls'
//             }
//         }

//         stage ('load script') {
//             steps {
//                 def code = load 'test_job.groovy'
//             }
//         }
//         stage('Groovy') {
//             steps {
//                 code.foo()
//             }
//         }
//         stage('End') {
//             steps {
//                 sh 'ls'
//             }
//         }
//     }
// }
def code
node(any) {
    stages {
        stage('Build') {
            steps {
            sh 'echo "This is my first step"'
            }
        }
        stage('Test') {
            steps
            sh 'echo "This is my Test step"'
            }
        }
        stage('Deploy') {
            steps {
            sh 'echo "This is my Deploy step"'
            }
        }
    }
}