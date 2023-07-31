pipeline {
    agent any 
    stages {
        stage('Verify java is installed or not') { 
            steps {
                sh "go version"
            }
            }
    
    stage('Build docker image') { 
            steps {
                    sh 'docker build -t go-image .'     
	                echo 'Build Image Completed'
                    sh 'docker images'
                }
        }
	stage('running container') { 
            steps {
                    sh 'docker run -td --name random jwt-app '     
	                echo 'Build Image Completed'
                    sh 'docker ps'
                }
        }
    }
}
