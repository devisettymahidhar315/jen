pipeline {
    agent any

    stages {
        stage('Deploy to Kubernetes') {
            steps {
                script {
                    sh "/usr/bin/kubectl apply -f deploy.yaml"
                }
            }
        }
    }

}
