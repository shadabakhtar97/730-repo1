pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    def dockerImage = docker.build('shadabubuntu1:latest')
                    args '-v /var/run/docker.sock:/var/run/docker.sock'
                    dockerImage.push()
                }
            }
        }
    }
}
