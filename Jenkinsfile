pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                  echo 'Hello World'
                  sshPublisher(publishers: [sshPublisherDesc(configName: 'DCS RCA Beta', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '''eval $(ssh-agent)
echo \'Borate71103!\' | sudo -S ssh-add /root/.ssh/su_dcs_coc
cd /var/www/html/rca
echo \'Borate71103!\' | sudo -S git pull''', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '', usePty: true)], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: true)])
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

