
pipeline {
    agent any

    stages {
        stage('Show Files') {
            environment {
              MY_FILES = sh(script: 'ls -la' , returnStdout: true)
            }
            steps {
              sh '''
                echo "$MY_FILES"
              '''
            }
        }
            
            
            
            
            }
        }





