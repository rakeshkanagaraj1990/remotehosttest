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
                        sh "scp -o StrictHostKeyChecking=no index.html 192.168.43.2"
                        }
                    }
                }
        }
    }
}
    
