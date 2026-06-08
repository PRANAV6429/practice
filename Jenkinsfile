pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                bat 'docker build -t my-nginx-image .'
            }
        }
        stage('Deploy'){
            steps{
                bat 'docker run -d -p 8000:80 --name my-nginx-container my-nginx-image'
            }
        }
    }
}