pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                sh 'sudo microk8s kubectl apply -f apache-deploy.yaml'
            }
        }
    }
}

