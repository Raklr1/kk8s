pipeline {
    agent any

    stages {
        stage('List Kubernetes Resources') {
            steps {
                withKubeConfig([credentialsId: 'k8s1']) {
                    sh 'kubectl get services --all-namespaces'
                    sh 'kubectl get deployments --all-namespaces'
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
