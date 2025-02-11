pipeline {
    agent any

    stages {
        stage('git') {
            steps {
                git 'https://github.com/hitaishi0622/devops-task.git'
            }
        }
        stage('build and run') {
            steps {
                sh '''docker build -f Dockerfile.java -t img1 .
                docker run --name java-container img1'''
            }
        }
    }
}
