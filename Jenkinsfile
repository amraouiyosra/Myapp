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
		

		
       
		      stage('build') { 
			   steps{
			      script{
				  sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"
			      		}
		          	}
		     		}

                      stage('Docker') {
                           steps{
                              script{
                                sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml"
                                }
                          }
                     }
		
                      stage('Docker-Registry') {
                           steps{
                              script{
                                sh "ansible-playbook ansible/docker-registry.yml -i ansible/inventory/host.yml"
                                }
                          }
                     }
               }


    }

	     
	     
