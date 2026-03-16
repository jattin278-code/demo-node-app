pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/jattin278-code/demo-node-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Application') {
            steps {
                sh 'node index.js'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t demo-node-app:latest .'
            }
        }

    }
}
