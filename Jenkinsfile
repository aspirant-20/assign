pipeline {

		agent {
		         label "built-in" 
			   }	     
		
		stages {
		
			stage ("23q1"){
			
				steps {
				
				    sh "cd /mnt/pratik" 
					sh "git checkout 23q1"
					//sh "docker stop 23q1"
					sh "docker system prune -a -f"
					sh "docker run -itdp 80:80 -v 23q1:/usr/local/apache2/htdocs --name 23q1 httpd"
					sh "docker cp index.html 23q1:/usr/local/apache2/htdocs"
					sh "docker exec 23q1 chmod -R 777 /usr/local/apache2/htdocs/index.html"
					
				
				}
			
			}
			stage ("23q2"){
			     steps {
				
				    sh "cd /mnt/pratik" 
					sh "git checkout 23q2"
					//sh "docker stop 23q2"
					sh "docker system prune -a -f"
					sh "docker run -itdp 90:80 -v 23q2:/usr/local/apache2/htdocs --name 23q2 httpd"
					sh "docker cp index.html 23q2:/usr/local/apache2/htdocs"
					sh "docker exec 23q2 chmod -R 777 /usr/local/apache2/htdocs/index.html"
			
				}
				
				    
			}
            stage ("23q3"){     
                  steps {
				
				    sh "cd /mnt/pratik" 
					sh "git checkout 23q3"
					//sh "docker stop 23q3"
					sh "docker system prune -a -f"
					sh "docker run -itdp 8081:80 -v 23q3:/usr/local/apache2/htdocs --name 23q3 httpd"
					sh "docker cp index.html 23q3:/usr/local/apache2/htdocs"
					sh "docker exec 23q3 chmod -R 777 /usr/local/apache2/htdocs/index.html"				
				}
			
			
			}
			
			
				
				
				   
				
				
			
			
		
		
		}



}
