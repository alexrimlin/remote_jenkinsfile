// pipeline {
//     agent any
//     stages {
//         stage ('first_stage') {
//             steps {
//                 echo "executing echo 1"
//             }
//         }
//         stage ('another_stage') {
//             steps {
//                 echo "reachable?"
//             }
//         }
//         stage ('failed_stage') {
//             steps {
//                 exit 0
//             }
//         }
//     }
// }
pipeline {
    agent any
    // {
    //     node {
    //             label 'main'
    //             customWorkspace 'refs/heads/master'
    //           }
    // }

    stages 
    {
        stage('Start') {
            steps {
                sh 'ls'
            }
        }

        stage ('Invoke_pipeline') {
            steps {
                sh 'echo invoking pipeline'
                build job: 'seed_job', parameters: [
                    string(name: 'param1', value: "value1")
                ]
            }
        }
        stage('Groovy') {
            steps {
                sh 'groovy test_job.groovy'
            }
        }
        stage('End') {
            steps {
                sh 'ls'
            }
        }
    }
}