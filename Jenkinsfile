pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo 'Building..'
				bat 'cd monappli & mvn install'
			}
		}
		stage('Test') {
			post {
                		success {
                    			junit '**/target/**/*.xml'
                        		}
                 		}
		}
		stage('Deploy') {
			steps {
				echo 'Deploying....'
			}
		}
	}
}
