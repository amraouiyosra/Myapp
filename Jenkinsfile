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
