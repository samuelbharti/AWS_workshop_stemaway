# AWS_workshop_stemaway






Installing Docker in your EC2 Instance:
```
sudo apt-get update
sudo apt-get install     ca-certificates     curl     gnupg     lsb-release

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo   "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com\
/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

Pulling and Running sMAP application in background at port 80 of your EC2 Instance:
```
sudo docker run --rm -d -p 80:80 samuelbharti/smap:latest
```






