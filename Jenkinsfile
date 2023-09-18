pipeline {
    agent any
    environment {
           TEST_URL = "google.com"
       }
    stages {
        stage('Compile') {
            steps {
                //echo 'Hello World'
                echo TEST_URL
            }
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
