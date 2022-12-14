pipeline {
    agent any

    stages {
         stage('STAGE1') {
             steps {
                 catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                 echo "stage 1 is running..."
                        sh 'sleep 5'
                 sh 'exit 1'
             }
             }
         }
                stage('STAGE2') {
                    steps {
                        echo "stage 2 is running..."
                        sh 'sleep 5'
             }
         }
            }
    }
    
//     stages {
//         stage('BUILD') {
//             steps {
//                 sh '''
//                 pwd
//                 sleep 5
//                 echo 'This is first stage:BUILD'
//                 '''
//             }
//         }
//         stage('TEST') {
//             parallel {
//                 stage('TEST1'){
//                     steps {
//                         sh 'sleep 5'
//                         echo "Testing Phase1"
//                     }
//                 }
//                 stage('TEST2'){
//                     steps {
//                         sh 'sleep 5'
//                         echo "Testing Phase2"
//                     }
//                 }
//                 stage('TEST3'){
//                     steps {
//                         sh 'sleep 5'
//                         echo "Testing Phase3"
//                     }
//                 }
//                 stage('TEST4'){
//                     steps {
//                         sh 'sleep 5'
//                         echo "Testing Phase4"
//                     }
//                 }
//             }
//         }
//         stage('DEPLOY') {
//             steps {
//                 sh '''
//                 pwd
//                 sleep 5
//                 echo 'This is first stage:DEPLOY'
//                 '''
//             }
//         }
//     }
// }

