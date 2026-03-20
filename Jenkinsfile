pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/sravs994/devops-demoprjct1.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app:latest .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5001:5001 devops-app:latest'
            }
        }
    }
}
