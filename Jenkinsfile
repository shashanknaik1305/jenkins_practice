pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-ssh',
                    url: 'git@github.com:shashanknaik1305/jenkins_practice.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'python3 --version'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'cat app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo "Pretending to deploy new version 🚀"
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded — code change integrated successfully!'
        }
        failure {
            echo '❌ Build failed — check your code or test!'
        }
    }
}
