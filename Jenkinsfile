pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                  echo 'Hello World'
                  sshPublisher(publishers: [sshPublisherDesc(configName: 'gateway', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'whoami', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/html/rca', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '', usePty: true)], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
        
        stage('Test') {
            steps {
                  echo 'Testing . . .'
            }
        }
        
        stage('Deploy') {
            steps {
                  echo 'Deploy!'
            }
        }
    }
}

