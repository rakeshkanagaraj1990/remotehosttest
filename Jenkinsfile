pipeline {
    agent none
    stages {
        stage('RemoteConnection') {
                agent any
                steps {
                    script {
                        sshagent (['remotehost']) {
                        sh "ssh -o StrictHostKeyChecking=no vagrant@192.168.43.2 hostname"
                        sh "scp -o StrictHostKeyChecking=no index.html vagrant@192.168.43.2:/home/vagrant"
                        }
                    }
                }
        }
    }
}
    
