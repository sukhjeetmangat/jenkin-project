def AGENT_LABEL=null
pipeline {

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
