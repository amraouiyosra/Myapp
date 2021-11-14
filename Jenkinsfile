 pipeline
   {

		agent any
		  stages {
		      stage('Pull') {
			   steps{
			      script{
				  checkout([$class: 'GitSCM', branches: [[name: '*/master']],
				      userRemoteConfigs: [[
					  credentialsId: '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',
					  url: 'https://github.com/amraouiyosra/Myapp.git']]])
			      }
		          }
		     }
		

		
        }
    }
	     
	     
