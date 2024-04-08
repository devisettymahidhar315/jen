pipeline {
    agent any
     stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "deploy.yaml", kubeconfigId: "kubernetes")
        }
      }
    }

  }

