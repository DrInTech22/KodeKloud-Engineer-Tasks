
# create a group
## Task
a. Create a group named nautilus_noc in all App servers in stratos Datacenter.

b. Add the user rajesh to nautilus_noc group in all App servers. (create user if doesn't exist).

## solution
1. ssh into the first server and create group nautilus_noc
```
groupadd nautilus_noc
```

2. Check if user exists
```
cat /etc/passwd | grep 'rajesh'
```

3. If user doesn't exist, create user and add it to the nautilus_noc group.
```
useradd rajesh
```
```
usermod -aG nautilus_noc
```
