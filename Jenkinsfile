
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
    stage('git clone') {
        sh 'git clone https://github.com/camelCat/remote_jenkinsfile.git'
    }   
    stage('load') {
        code = load 'test_job.groovy'
    }
    stage('execute') {
        code.foo()
    }
}