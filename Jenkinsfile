// pipeline {
//     //agent any
//     agent {node { label 'workstation' }}
//         options {
//             ansiColor('xterm')
//         }
//             parameters {
//                 string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//
//                 text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//
//                 booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//
//                 choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//
//                 password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//             }
//                 tools {
//                     maven 'maven'
//                 }
//             triggers { pollSCM('*/10 * * * *') }
//             //Prakash Tammala
//
//
//
//     environment {
//         Test_URL = "google.com"
//         SSH = credentials("centos-ssh")
//     }
//
//     stages {
//         stage('Compile') {
//                     when {
//                         branch 'production'
//                     }
//         input {
//                                     message "Should we continue?"
//                                     ok "Yes, we should."
//
//                                     //Prakash
//                                 }
//
//             steps {
//                 echo Test_URL
//                 echo SSH
//                 sh 'env'
//                 sh 'ansible -i 3.86.64.152, all  -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
//                 sh 'mvn -v'
//
//             }
//         }
//     }
//     post{
//     always{
//     echo 'post'
//     //send email
//     //trigger from anther job
//     //Update some jira status
//     }
//
//     }
// }
//
// pipeline {
//     agent any
//     stages {
//         stage('Non-Parallel Stage') {
//             steps {
//                 echo 'This stage will be executed first.'
//             }
//         }
//         stage('Parallel Stage') {
// //             when {
// //                 branch 'master'
// //             }
//             failFast true
//             parallel {
//                 stage('Branch A') {
//                     agent {
//                         label "for-branch-a"
//                     }
//                     steps {
//                         echo "On Branch A"
//                     }
//                 }
//                 stage('Branch B') {
//                     agent {
//                         label "for-branch-b"
//                     }
//                     steps {
//                         echo "On Branch B"
//                     }
//                 }
//                 stage('Branch C') {
//                     agent {
//                         label "for-branch-c"
//                     }
//                     stages {
//                         stage('Nested 1') {
//                             steps {
//                                 echo "In stage Nested 1 within Branch C"
//                             }
//                         }
//                         stage('Nested 2') {
//                             steps {
//                                 echo "In stage Nested 2 within Branch C"
//                             }
//                         }
//                     }
//                 }
//             }
//         }
//     }
// }

def samplef()
{
print "xyz in funxtion"
}
node ('workstation'){
    def x = 10
    env.y = 20
    if ( x > 10 ){
        stage('Test'){
        print x
        sh 'echo y - ${y}'
        samplef()
    }
    }
    else{
    stage('Test1'){
    samplef()
    }
    }
    }