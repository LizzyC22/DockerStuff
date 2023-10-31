# DockerStuff
# Wordpress installed via Docker Compose Documentation  
<font color="gold"> Elizabeth Christensen </font>  
<font color="white"> Starting off with installing Docker and Docker Compose on Ubuntu, run the following commands from https://docs.docker.com/engine/install/ubuntu/  
  
Add Docker's official GPG key:  
sudo apt-get update  
sudo apt-get install ca-certificates curl gnupg  
sudo install -m 0755 -d /etc/apt/keyrings  
curl -fsSL https://download.docker.com/linux/ubuntu/  
gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg  
sudo chmod a+r /etc/apt/keyrings/docker.gpg  
  
Add the repository to Apt sources:  
echo \
  "deb [arch="\$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null  
sudo apt-get update  
  
Obtain a updated version as well >  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


  
Following this set of commands, we move onto the installation of Wordpress.  
<font color="royalblue"> 
# Wordpress Server via Docker  </font>  

touch docker-compose.yml
  
nano docker-compose.yml  

insert the following script found in this github link, which is also in the resources >  
https://github.com/docker/awesome-compose/blob/master/wordpress-mysql/compose.yaml

  After saving this to the file, run >  
sudo docker compose up -d  

  
    
  
<font color="royalblue"> 
Resources  </font>   

https://docs.docker.com/engine/install/ubuntu/  
https://docs.docker.com/samples/wordpress/  
https://github.com/docker/awesome-compose/blob/master/wordpress-mysql/compose.yaml  

</font>  
