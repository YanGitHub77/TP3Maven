pipeline {
	agent any
    	tools {
        	maven 'maven3.5.3'
        	jdk 'jdk 11'
    	}
	stages {
		stage ('Initialize') {
            		steps {
                		bat '''
                    		echo "PATH = %PATH%"
                    		echo "M2_HOME = %M2_HOME%"
                		'''
            		}
        	}
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
