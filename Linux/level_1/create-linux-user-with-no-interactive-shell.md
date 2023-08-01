
# Create a Linux User with non-interactive shell
The System admin team of xFusionCorp Industries has installed a backup agent tool on all app servers. As per the tool's requirements they need to create a user with a non-interactive shell.

## Task
a.  create a user named yousuf with a non-interactive shell on the App Server 3.

## solution
1. ssh into the App server 3 
```
ssh username@ip_addr
```

2. create a user yousuf with non interactive shell
```
adduser yousuf -s /sbin/nologin
```

3. To confirm user is created with the above requirements
```
cat /etc/passwd | grep yousuf
```

