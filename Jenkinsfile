pipeline {
    agent any

    stages {
        stage('BUILD') {
            steps {
                sh '''
                pwd
                sleep 5
                echo 'This is first stage:BUILD'
                '''
            }
        }
        stage('TEST') {
            steps {
                sh '''
                pwd
                sleep 5
                echo 'This is first stage:TEST'
                '''
            }
        }
        stage('DEPLOY') {
            steps {
                sh '''
                pwd
                sleep 5
                echo 'This is first stage:DEPLOY'
                '''
            }
        }
    }
}
