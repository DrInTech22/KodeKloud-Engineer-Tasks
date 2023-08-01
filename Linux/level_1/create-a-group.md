
# create a group
## Task
a. Create a group named nautilus_noc in all App servers in stratos Datacenter.

b. Add the user rajesh to nautilus_noc group in all App servers. (create user if doesn't exist).

![Screenshot (4)](https://github.com/Dr1nTech/KodeKloud-Engineer-Tasks/assets/94924061/fbb9d35e-5a38-4e44-afd0-6597fa355223)


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

![Screenshot (5)](https://github.com/Dr1nTech/KodeKloud-Engineer-Tasks/assets/94924061/f162aeb6-c7f2-4753-ba03-757bdd34d18a)

```
useradd rajesh
```
```
usermod -aG nautilus_noc
```
