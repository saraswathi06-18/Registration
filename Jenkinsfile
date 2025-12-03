
pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker Image'
                bat 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                echo 'Running Docker Container'
                bat 'docker run -d -p 5000:5000 --name mycontainer myapp'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Successful'
        }
        failure {
            echo 'Pipeline Failed'
        }
    }
}
