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
        stage('Build') {

            
            try {
                def dir1 = sh(script:"ls -la  2>${stderrfile}", returnStdout:true).trim()
            } catch (Exception ex) {
                def errmsg = readFile(stderrfile)
                println("Unable to read dir1: ${ex} - ${errmsg}")
            }
            
            
            
            
            
            }
        }
    }
}



