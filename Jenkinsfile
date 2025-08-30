pipeline {
    agent any

    stages {
        stage('List Kubernetes Resources') {
            steps {
                withKubeConfig([credentialsId: 'k8s1']) {
                    bat 'kubectl get services --all-namespaces'
                    bat 'kubectl get deployments --all-namespaces'
                }
            }
        }
    }

    post {
        always {
            echo "Kubernetes 列表查询完成"
        }
    }
}
