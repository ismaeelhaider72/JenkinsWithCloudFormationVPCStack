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
            steps {
                sh "ls -l > commandResult"
                result = readFile('commandResult').trim()
            }
        }
    }
}



