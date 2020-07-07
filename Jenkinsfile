pipeline {
    agent none
    stages {
        stage('RemoteConnection') {
                agent any
                }
                steps {
                    script {
                        sshagent (['remotehost']) {
                        sh "scp -o StrictHostKeyChecking=no index.html 192.168.43.2"
                        }
                    }
                }
        }
    }
}
    
