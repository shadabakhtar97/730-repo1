pipeline {
    agent any

    environment {
        DOCKER_REGISTRY = "docker.io"
        DOCKER_IMAGE = "shadabakhtar/ubuntu:latest"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build shadabakhtar/ubuntu:latest
                }
            }
        }

   stage('Push to Docker Hub') {
      steps {
        script {
          docker.withRegistry('https://registry.hub.docker.com', registryCredential) {
            dockerImage.push("${shadabakhtar/ubuntu:latest}")
          }
        }
      }
    }

                }
    }
}
