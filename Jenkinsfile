pipeline {
    agent any
    parameters {
//         password()
//         text()
//         booleanParams()
        //string(name: "TARGET_ENV", description: "target environment to deploy")
        choice(name: "TARGET_ENV", choices: ['test', 'prod'], description: "target environment to deploy")
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
    post {
        always{
        echo "you can see always"
        }
    }
}

