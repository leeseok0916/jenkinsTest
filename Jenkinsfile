// 레파지토리 소스에 Jenkinsfile 만들고 그걸 실행시켜보기
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

// 도커 파일을 이용해서 도커 이미지 생성하기
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
