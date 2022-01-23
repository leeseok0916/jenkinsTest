// pipeline {
//     agent any
    
//     stages() {
//         stage('git clone') {
//             steps() {
//                 git 'https://github.com/leeseok0916/jenkinsTest.git'
//             }
//         }
        
//         stage('Test') {
//             steps {
//                 echo 'Testing..'
//             }
//         }
        
//         stage('execute sh') {
//             steps {
//                 sh "chmod 774 ./project.sh"
//                 sh "./project.sh"
//             }
//         }        
//     }
// }

pipeline {
    agent any
    
    stages() {
        stage('git clone') {
            steps() {
                git 'https://github.com/leeseok0916/jenkinsTest.git'
            }
        }
        
        stage('create docker image') {
            steps {
                sh "docker build -t app-for-jenkins-test:0.0.1  --network host ."
            }
        }
    }
}
