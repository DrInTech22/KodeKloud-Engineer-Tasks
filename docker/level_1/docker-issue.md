
# Docker Container Issue


There is a static website running within a container named nautilus, this container is running on App Server 1. Suddenly, we started facing some issues with the static website on App Server 1. Look into the issue to fix the same, you can find more details below:
## Task
1. Container's volume /usr/local/apache2/htdocs is mapped with the host's volume /var/www/html.

2. The website should run on host port 8080 on App Server 1 i.e command curl http://localhost:8080/ should work on App Server 1.

## solution
1. login to app server 1

```
ssh username@ip_addr
```

2. check status of nautilus container
```
docker ps -a
```

3. Restart nautilus container
```
docker restart nautilus
```
