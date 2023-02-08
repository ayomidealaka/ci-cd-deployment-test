pipeline {
    agent any

    stages {
        stage('Print Hello World') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Cloning Git') {
            steps {
                sh 'rm -fr ci-cd-deployment-test'
                sh 'git clone https://github.com/ayomidealaka/ci-cd-deployment-test.git'
            }
        }
    }
}
