pipeline {
    agent any
    environment {
           TEST_URL = "google.com"
           SSH = credentials("centos-ssh")
       }
       options {
               ansiColor('xterm')
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
