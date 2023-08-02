
# Linux User Without Home
The system admins team of xFusionCorp Industries has set up a new tool on all app servers, as they have a requirement to create a service user account that will be used by that tool.





## Task
a. Create a user named ammar in App Server 2 without a home directory.

## solution
1. ssh into the App server 2
```
ssh username@ip_addr
```

2. create a user yousuf with no home directory with -M option
```
useradd -M ammar
```

3. To confirm user is created with the above requirements
```
cat /etc/passwd | grep ammar
```
```
ls /home
```

