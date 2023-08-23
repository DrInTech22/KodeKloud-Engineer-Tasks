
# Install Docker Package


Last week the Nautilus DevOps team met with the application development team and decided to containerize several of their applications. The DevOps team wants to do some testing per the following:

## Task
1. Install docker-ce and docker-compose packages on App Server 2.


2. Start docker service.

![Screenshot (44)](https://github.com/DrInTech22/KodeKloud-Engineer-Tasks/assets/94924061/690f4bfb-ed35-4bd2-b354-f61329b56ee8)


## solution
1. login to app server 1 and switch to root user

```
ssh username@ip_addr
```
  switch to root user
```
sudo su
```

2. Install docker-ce using yum package manager
```
sudo yum install docker-ce
```
Note: Docker repository key has been added to the system by default

3. add user to docker group
```
sudo usermod -aG docker $USER
```
```
newgrp docker
```
This enables user to run docker operations without sudo command 


4. start docker service
```
sudo systemctl start docker
```
```
docker --version 
```
5. Install docker-compose and grant execution permission to it.

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```
sudo chmod +x /usr/local/bin/docker-compose
```
```
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

6. confirm docker-compose is installed
```
docker-compose --version
```

