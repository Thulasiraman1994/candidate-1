pipeline {
    agent any

    stages {
        stage('Creating Docker Image') {
            steps {
                sh '''
                sudo docker build -t nodejs:webapp . 
                '''
            }
        }
        stage('Deploying Docker Image') {
          steps {
                sh '''
                sudo docker run -p 8080:8080 -d nodejs:webapp
                '''
          }
        }
    }
}
