pipeline {
    agent any
    triggers{
        cron('H/2 ****')
    }
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
        stage('run') {
            steps {
                sh 'docker run -d flaskapp2:v1'
            }
        }
    }
}
