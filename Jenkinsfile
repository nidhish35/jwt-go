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
	stage('building container') { 
            steps {
                    sh 'docker run -td jwt-app go-image'     
	                echo 'Build Image Completed'
                    sh 'docker images'
                }
        }
    }
}
