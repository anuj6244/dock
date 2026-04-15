pipeline {
    agent any

    stages {
        stage('Clone Code') {
    steps {
        echo 'Code already checked out'
    }
}

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-web-app:v1 .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name webapp my-web-app:v1'
            }
        }
    }
}
