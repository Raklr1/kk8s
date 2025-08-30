pipeline {
    agent any

    environment {
        KUBECONFIG = "/var/lib/jenkins/.kube/config"
    }

    stages {
        stage('Check kubectl version') {
            steps {
                echo 'Checking kubectl version...'
                sh 'kubectl version --client'
            }
        }

        stage('List Kubernetes Nodes') {
            steps {
                echo 'Listing Kubernetes nodes...'
                sh 'kubectl get nodes'
            }
        }

        stage('List Pods in Default Namespace') {
            steps {
                echo 'Listing pods in default namespace...'
                sh 'kubectl get pods'
            }
        }
