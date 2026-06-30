pipeline {
    agent any
    stages {
        stage('clone') {
            steps {
                git 'https://github.com/Prathap023/inter-flask.git'
            }
        }
        stage('DOcker Build') {
            steps {
                sh 'docker build -t flaskapp2:v1 .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}
