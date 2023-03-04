pipeline{
    agent any

    stages {

        stage('Deploy Kubernetes') {
            agent {
                kubernetes {
                    cloud 'kubernetes'
                }
            }

            steps {
                kubernetesDeploy(config: '**/k8s/**', kubeconfigId: 'kubeconfig')
            }
        }
    }
}
