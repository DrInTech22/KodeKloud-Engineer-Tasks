
# Linux User Files
There was some users data copied on Nautilus App Server 2 at /home/usersdata location by the Nautilus production support team in Stratos DC. Later they found that they mistakenly mixed up different user data there. Now they want to filter out some user data and copy it to another location. Find the details below:


## Task
a. On App Server 2 find all files (not directories) owned by user john inside /home/usersdata directory and copy them all while keeping the folder structure (preserve the directories path) to /ecommerce directory.


## solution
1. ssh into the App server 2
```
ssh username@ip_addr
```
2. List all files under userdata directory owned by user john
```
find /home/usersdata -type f -user john
```

3. copy all files owned by user john to /ecommerce directory while keeping the folder structure
```
find /home/usersdata -type f -user john -exec cp --parents {} /ecommerce \;
```
4. confirm your work
```
ls -l /ecommerce 
```
### Note: all files under /ecommerce are owned by john but the parent directory and sub directories might be owned by root user or any other user.



