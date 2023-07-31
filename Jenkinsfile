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
    }
}
