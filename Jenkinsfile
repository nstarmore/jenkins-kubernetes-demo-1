pipeline {
    agent any
    stages {
        stage ('Deploy Backend') {
            steps {
                sh "kubectl apply -f backend.yaml"
            }
        }
        stage ('Deploy Frontend') {
            steps {
                sh "kubectl apply -f frontend.yaml"
                sh "kubectl get svc"
                sh "sleep 60"
                sh "kubectl get svc svc frontend"
            }
        }
    }
}