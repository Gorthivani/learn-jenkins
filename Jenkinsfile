pipeline {
    agent any
    environment {
           TEST_URL = "google.com"
           SSH = credentials("centos-ssh")
       }
    options {
               ansiColor('xterm')
               }
    parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

            text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

            booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

            choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

            password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
        }
    triggers
    {
         pollSCM('*/1 * * * *')
      }
    stages {
        stage('Compile') {
            steps {
                //echo 'Hello World'
                echo TEST_URL
                echo SSH
                sh 'env'
                sh 'ansible -i 172.31.30.126, all -e ansible_user=$(SSH_USR) -e ansible_password=$(SSH_PSW) -m ping'            }
        }


        stage('Test') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Code Quality') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Code Security') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
// pipeline {
//     agent any
//     stages {
//         stage('Non-Parallel Stage') {
//             steps {
//                 echo 'This stage will be executed first.'
//             }
//         }
//         stage('Parallel Stage') {
//             when {
//                 branch 'main'
//             }
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