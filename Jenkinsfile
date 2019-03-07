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
  	}git commit -m "first commit"
  	post {
    	always {
        	archiveArtifacts artifacts: 'log/*', allowEmptyArchive: true
        	cleanWs()
    	}
  	}
}
