pipeline {
    agent any
    stages {
        stage("Deploy") {
            steps {
                sh '''
                kubectl apply -f frontend.yaml
				echo "frontend yaml applied"
				sleep 10
				kubectl apply -f backend.yaml
				echo "backend yaml applied"
                sleep 60
                kubectl get services
                '''
            }
        }
    }
}
