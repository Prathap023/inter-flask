pipeline {
    agent any
    
    triggers {
        cron('H/2 * * * *')
    }
    
    stages {
        stage('Clone') {
            steps {
                git branch: 'master', url: 'https://github.com/Prathap023/inter-flask.git'
            }
        }
        
        stage('Docker Build') {
            steps {
                sh 'docker build -t flaskapp2:v1 .'
            }
        }
        
        stage('Docker Run') {
            steps {
                sh '''
                    docker run -d --name my-flask-app -p 5000:5000 flaskapp2:v1
                '''
            }
        }
    }
}
