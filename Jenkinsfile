pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/flask-ci-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'python -m pip install --upgrade pip'
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'python -m unittest discover'
            }
        }

        stage('Docker Build & Push') {
            steps {
                script {
                    dockerImage = docker.build("Junyan714/flask-ci-app:latest")
                    docker.withRegistry('https://registry.hub.docker.com', 'dckr_pat_I_j3eW5YDX8FZ5MjjW1Z8SYfFSI') {
                        dockerImage.push()
                    }
                }
            }
        }
    }
}
