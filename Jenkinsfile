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
    //             customWorkspace "."
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
                build job: 'seed_job', parameters: [
                    string(name: 'param1', value: "value1")
                ]
                sh 'invoking pipeline'
            }
        }

        stage('End') {
            steps {
                sh 'ls'
            }
        }
    }
}