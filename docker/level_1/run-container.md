
# Run a Docker Container


Nautilus DevOps team is testing some applications deployment on some of the application servers. They need to deploy a nginx container on Application Server 2. Please complete the task as per details given below:

## Task
1. On Application Server 2 create a container named nginx_2 using image nginx with alpine tag and make sure container is in running state.

## solution
1. login to app server 2 and switch to root user

```
ssh username@ip_addr
```
  switch to root user
```
sudo su
```

2. Confirm docker-daemon is up and running
```
service docker status
```

3. run the docker container with specified name and image tag
```
docker run -d --name nginx_2 nginx:alpine
```
- -d(detached mode): runs the docker container underground.
- --name: declares the name of the container

4. validate the success of your task
```
docker ps
```



