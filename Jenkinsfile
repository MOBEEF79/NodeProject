pipeline {
    agent any
    stages {
        stage('Init'){
            steps {
                sh "docker rm -f mynodeapp"
            }
        }
        stage('Build'){
            steps {
                sh "docker build -t nodeapp:latest ."
            }
        }
        stage('Deploy'){
            steps {
                sh "docker run -d -p 5000:5000 --name mynodeapp nodeapp:latest"
            }
        }
    }
}
