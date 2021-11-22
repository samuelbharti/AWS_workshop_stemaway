# AWS Deployment of R Shiny Bioinformatics App hosted by [STEM-AWAY](https://stemaway.com/)
> An example of [sMAP: Standard Microarray Analysis Pipeline](https://github.com/BI-STEM-Away/sMAP).

### Launching an EC2 Instance from your AWS Management Console dashboard

A snapshot demo of launching an AWS EC2 Instance is described [here](AWS_EC2_launch_and_connect).



### Installing Docker in your EC2 Instance:

```Shell
sudo apt-get update
```

```Shell
sudo apt-get install     ca-certificates     curl     gnupg     lsb-release
```

```Shell
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

```Shell
echo   "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com\
/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```Shell
sudo apt-get update
```

```Shell
sudo apt-get install docker-ce docker-ce-cli containerd.io
```


### Pulling and Running sMAP application in background at port 80 of your EC2 Instance:

```Shell
sudo docker run --rm -d -p 80:80 samuelbharti/smap:latest
```


### Post-deployment: Demo of sMAP

A snapshot demo of sMAP analysis is described [here](sMAP_demo).

https://docs.google.com/viewer?url=https://github.com/samuelbharti/AWS_workshop_stemaway/sMAP_demo.pptx

