pipeline {
    agent any
    
   

    stages {
        
    stage('Deploy to Kubernetes') {
            steps {
                script {
                    sh "kubectl apply -f deploy.yaml"
                }
            }
        }
    }
}
