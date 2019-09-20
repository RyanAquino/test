pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                  echo 'Hello World'
                  sh 'ssh a-ryanaq@dcs-b-cocportal01.sjc1 hostname'
                  sh "ssh -t a-ryanaq@dcs-b-cocportal01.sjc1 'cd /var/www/html/rca ; sudo git fetch ;'"
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

