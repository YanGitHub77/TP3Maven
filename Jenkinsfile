pipeline {
	agent any
	stages {
		stage('Build and Test' ) {
			steps {
				echo 'Building..'
				bat 'cd monappli & mvn install'
				echo 'Fin Building..'
			}
			post {
				echo 'Test..'
                		success {
                    			junit '**/target/**/*.xml'
                        		}
                 		}
				echo 'Fin Test..'
		}
		stage('Deploy') {
			steps {
				echo 'Deploying....'
			}
		}
	}
}
