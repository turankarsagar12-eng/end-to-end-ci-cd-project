
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code will be checked out by Jenkins.'
            }
        }

        stage('Validate Files') {
            steps {
                sh 'test -f index.html'
                sh 'test -f style.css'
                sh 'test -f Dockerfile'

                echo 'All required project files are present.'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-cicd-website .'
            }
        }
    }
}

