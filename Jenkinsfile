pipeline {
    agent any

    stages {
        stage('Permission') {
            steps {
                sh '''
		sudo usermod -a -G microk8s jenkins
		sudo chown -R jenkins ~/.kube
		newgrp microk8s
		'''
            }
        }
        stage('Deploy') {
            steps {
                sh 'microk8s kubectl apply -f apache-deploy.yaml'
            }
        }
    }
}

