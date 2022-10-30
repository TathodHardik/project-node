pipeline{

agent{
    label{
           label'10.0.1.204'
		   customWorkspace"/mnt/deploy"
	}
	}
   stages{
         
		 
      stage('install-docker-compose'){
	          steps{ 
			   sh"sudo chmod 777 docker-compose-install.sh "
			   sh"sudo ./docker-compose-install.sh"
			   }
	  }
      stage('run-docker-compose'){
	     steps{
		     sh"sudo docker-compose down"
			 sh"sudo docker system prune -a -f "
		     sh"sudo docker-compose up -d --scale service-tomcat=2"
		 
		 }
	  }
   }
  
  
  
  
  
  } 
 
