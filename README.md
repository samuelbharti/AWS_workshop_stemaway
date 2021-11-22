# AWS Deployment of R Shiny Bioinformatics App 
> An example of sMAP: Standard Microarray Analysis Pipeline 

### Launching an EC2 Instance from your AWS Management Console dashboard

### Installing Docker in your EC2 Instance:

1. ```sudo apt-get update```

2. `sudo apt-get install     ca-certificates     curl     gnupg     lsb-release`

3. `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`

4. `echo   "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com\
/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

5. `sudo apt-get update`

6. `sudo apt-get install docker-ce docker-ce-cli containerd.io`


### Pulling and Running sMAP application in background at port 80 of your EC2 Instance:

7. `sudo docker run --rm -d -p 80:80 samuelbharti/smap:latest`


### Post-deployment: Demo of sMAP



