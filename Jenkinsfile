pipeline {
    agent none
    stages {
        stage('RemoteConnection') {
                agent any
                options {
                    skipDefaultCheckout(true)
                }
                steps {
                    script {
                        sshagent (credentials: ['remotehost']) {
                        sh 'ssh -o StrictHostKeyChecking=no -l vagrant 192.168.43.2 hostname'
                        }
                    }
                }
        }
    }
}
    
