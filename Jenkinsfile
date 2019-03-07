pipeline {
  agent any

	options {
  	timestamps()
	}

  	stages {
    	stage('Mobile Test') {
      		steps {
            	sh "./test.sh"
      		}
    	}
  	}
  	post {
    	always {
        	archiveArtifacts artifacts: 'log/*', allowEmptyArchive: true
        	cleanWs()
    	}
  	}
}
