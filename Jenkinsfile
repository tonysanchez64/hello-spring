pipeline {
    agent any

    stages {
	stage('Compile'){
            steps{
		sh './mvnw package'
            }
	}
        stage('Build'){
            steps{
                sh 'docker-compose build'
            }
        }
        stage('deploy'){
            steps{
                sh 'docker-compose up -d'
            }
        }
          
    }
    
}

