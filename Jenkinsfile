def stderrfile = 'stderr.out'
pipeline {
    agent {
        label '!windows'
    }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

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





