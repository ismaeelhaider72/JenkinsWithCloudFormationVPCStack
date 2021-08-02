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
        stage('stage1'){
        def commit = sh (returnStdout: true, script: '''echo hi
        echo bye | grep -o "e"
        date
        echo lol''').split()


        echo "${commit[-1]} "

        }
            
            
            
            
            
            }
        }
    }




