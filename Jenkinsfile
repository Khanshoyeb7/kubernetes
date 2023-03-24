pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                sh 'microk8s kubectl apply -f apache-deploy.yaml'
            }
        }
    }
}

