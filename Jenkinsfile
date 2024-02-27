pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    def dockerImage = docker.build('shadabubuntu1:latest')
                    dockerImage.push()
                }
            }
        }
    }
}
