ipeline {

    agent {
        docker {	image 'apache2-18059906-image'
        }
    }


    environment {
        APP_ID = "18059906"
        APP_ENV  = "DEV"
    }

    stages {
        
        stage('Stage1 - 18059906') {
            steps {
                echo "Stage 1 Completed -  ${APP_ID}"
                
            }
        }
	parallel {

	        stage('Stage2 - 18059906') {
        	    steps {
                	checkout([
                    	$class: 'GitSCM', 
                    	branches: [[name: '*/main']], 
                    	userRemoteConfigs: [[url: 'https://github.com/jayzlin/Jenkinsfile.git']]
               	 ])
			echo "Stage 2 Completed - ${APP_ID}"
            	}
        }

        	stage('Stage3 - 18059906') {
       			steps {
                		echo "Stage 3 Completed - ${APP_ID}"
            }
        }

        stage('Stage4 - 18059906') {
            steps {
               	sh """
                env
                """
            }
        }

	stage('Stage5 - 18059906') {
            steps {
                sh """
                env
                """
            }
        }
			
    }   
}
