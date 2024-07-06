pipeline {
    agent any

    environment {
        NODE_ENV = 'production'
        PORT = '3000'
    }

    stages {
        stage('Code Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Static Code Analysis') {
            steps {
                // Añadir herramientas de análisis estático como ESLint
                sh 'npm run lint'
            }
        }
        stage('Code Coverage') {
            steps {
                // Añadir herramientas de cobertura de código
                sh 'npm run coverage'
            }
        }
    }
}
