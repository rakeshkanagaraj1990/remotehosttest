pipeline {
    agent none
    stages {
        stage('RemoteConnection') {
                agent any
                steps {
                    script {
                        sshagent (['remotehost']) {
                        sh "ssh -o StrictHostKeyChecking=no -l vagrant 192.168.43.2 hostname"
                        sh "scp -o StrictHostKeyChecking=no -l vagrant index.html 192.168.43.2:/home/vagrant"
                        }
                    }
                }
        }
    }
}
    
