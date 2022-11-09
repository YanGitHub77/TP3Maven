pipeline {
	agent any
    	tools {
        	maven 'Maven3.5.3'
        	jdk 'java11'
    	}
	stages {
		stage('Build and Test' ) {
			steps {
				echo 'Building..'
				bat 'cd monappli & mvn install'
				echo 'Fin Building..'
			}
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
