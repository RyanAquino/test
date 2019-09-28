pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                  echo 'Hello World'
                  sshPublisher(publishers: [sshPublisherDesc(configName: 'DCS Beta', sshCredentials: [encryptedPassphrase: '{AQAAABAAAAAQsvdN7Q2EUe56IijqzHmRud5uLyLoCXl8X1MKrKR6h90=}', key: '', keyPath: '', username: 'a-ryanaq'], transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '''cd /var/www/html/rca
sudo git pull
echo \'Borate71103!\' | sudo -S git pull
ls''', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '', usePty: true)], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
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

