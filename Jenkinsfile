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
                        sshagent (['remotehost']) {
                        sh "scp -o StrictHostKeyChecking=no ${WORKSPACE}/index.html 192.168.43.2"
                        }
                    }
                }
        }
    }
}
    
