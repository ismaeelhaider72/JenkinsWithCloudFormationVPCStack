pipeline {
    agent any
    stages {

            
        stage('Show Files') {
            environment {
              MY_FILES = sh(script: 'ls -l', returnStdout: true)
            }
            steps {
              sh '''
                echo "$MY_FILES"
              '''
            }
        }            
             }
            }
