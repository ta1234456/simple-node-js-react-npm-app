pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                echo 'Build'
                bat 'docker build -t todo-app .'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploy the TODO application on Docker'
                bat 'docker run -p 8000:8000 -d todo-app'
            }
    }
}
