pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build Stage'
            }
        }
stage('Test') {
            steps {
                echo 'Test Stage'
            }
        }
stage('UAT') {
            steps {
                echo 'UAT Stage'
            }
        }
stage('Production') {
            steps {
                echo 'Production Stage'
            }
        }
    }
}
