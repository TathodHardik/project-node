pipeline{

agent{
    label{
           label'10.0.4.187'
		   customWorkspace"/mnt/deploy"
	}
	}
   stages{
      stage('install-docker-compose'){
	          steps{ 
			   sh"sudo ./docker-compose-install.sh"
			   }
	  }
      stage('run-docker-compose'){
	     steps{
		     sh"docker-compose up -d --scale service-tomcat=2"
		 
		 }
	  }
   }
  
  
  
  
  
  } 
 
