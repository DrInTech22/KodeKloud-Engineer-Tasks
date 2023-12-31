# Docker Copy Operations

The Nautilus DevOps team has some confidential data present on App Server 3 in Stratos Datacenter. There is a container ubuntu_latest running on the same server. We received a request to copy some of the data from the docker host to the container. Below are more details about the task:

## Task
On App Server 3 in Stratos Datacenter copy an encrypted file /tmp/nautilus.txt.gpg from docker host to ubuntu_latest container (running on same server) in /opt/ location. Please do not try to modify this file in any way.


## solution
1. login to app server 3 

```
ssh username@ip_addr
```

2. Use the `docker cp` command to copy file from host to docker container
```
docker cp /tmp/nautilus.txt.gpg ubuntu_latest:/opt/
```
3. Confirm task success
```
docker attach <containerId>
```
```
ls /opt/
```
