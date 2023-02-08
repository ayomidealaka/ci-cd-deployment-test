// pipeline {
//     agent any
    
//     triggers {
//         githubPush()
//     }

//     stages {
//         stage('Print Hello World') {
//             steps {
//                 echo 'Hello World'
//             }
//         }
//         stage('Cloning Git') {
//             steps {
//                 sh 'rm -fr ci-cd-deployment-test'
//                 sh 'git clone https://github.com/ayomidealaka/ci-cd-deployment-test.git'
//             }
//         }
//     }
// }

pipeline {
    agent any
    stages {
        /* "Build" and "Test" stages omitted */

        stage('Deploy - Staging') {
            steps {
                echo 'Deploying to Staging'
                echo 'Staging deployed'
                echo 'Running smoke tests'
                echo 'Smoke test passed'
            }
        }

        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }

        stage('Deploy - Production') {
            steps {
                echo 'Deploying to production'
                echo 'Production deployed'
            }
        }
    }
}
