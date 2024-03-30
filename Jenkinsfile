pipeline {
    agent any

    stages {
        stage('Test Stage') {
            steps {
                script {
                    bat 'docker info'
                }
            }
        }

        stage('Build Stage') {
            steps {
                script {
                    bat 'docker build -t my-py1-app .'
                }
            }
        }

        stage('Deploy Stage') {
            steps {
                script {                    
                  
                  bat 'docker run -d --name my-py1-container my-py1-app'
                    // Fetch the output of the java script
		    
                  bat 'docker logs my-py1-container'
                }
            }
        }
    }
}