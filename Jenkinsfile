pipeline {
    agent any
    parameters {
        string(name: "TARGET_ENV", description: "target environment to deploy")
    }
    environment {
        DEPLOY_TO = "${TARGET_ENV}"
    }
    stages {
        stage("DEPLOY_TEST"){
            when {
                environment name: "DEPLOY_TO", value:"test"
            }
            steps {
                echo "DEPLOY to test environment..."
                sh 'sleep 5'
            }
        }
         stage("DEPLOY_PROD"){
            when {
                environment name: "DEPLOY_TO", value:"prod"
            }
            steps {
                echo "DEPLOY to production environment..."
                sh 'sleep 5'
            }
        }
    }
}

