pipeline {
    agent any

    stages {
        stage('List') {
            steps {
                   sh "ls"
            }
        }
        
        stage('Deploy') {
            steps {
                withKubeConfig(caCertificate: '', clusterName: '', contextName: '', credentialsId: 'kube-config-two', namespace: '', restrictKubeConfigAccess: false, serverUrl: 'https://192.168.0.113:16443') {
                    sh "kubectl apply -f ."
                }
            }
        }
    }
}
