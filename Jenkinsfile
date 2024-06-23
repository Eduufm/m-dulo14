pipeline {
    agent any
    stages {
        stage('Clonar o repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/Eduufm/m-dulo14'
            
            }
        }
        stage('instalar dependencias') {
            steps {
                bat 'npm install'
            }
        }
        stage('Executar Testes') {
            steps {
                bat 'NO_COLOR=1 npm run cy:run'
            }
        }
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
    }
}