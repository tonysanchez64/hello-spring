pipeline {
    agent any

    stages {
	stage('Build'){
            steps{
		sh './mvnw package'
		sh 'docker-compose build'
            }
	}
	post{
		always{
			junit 'target/surefire-reports/*.xml'
		}
	}
        stage('deploy'){
            steps{
                sh 'docker-compose up -d'
            }
        }
          
    }
    
}

