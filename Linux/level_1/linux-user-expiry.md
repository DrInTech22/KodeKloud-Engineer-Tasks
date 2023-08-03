
# Linux User Expiry
A developer named mark has been assigned Nautilus project temporarily as a backup resource. As a temporary resource for this project, we need a temporary user for mark. It’s a good idea to create a user with an expiration date so that the user won't be able to access servers beyond that point.


## Task
a. create a user named mark on the App Server 1 in Stratos Datacenter.

b. Set expiry date to 2021-01-28. Make sure the user is created as per standard and is in lowercase.

![Screenshot (18)](https://github.com/DrInTech22/KodeKloud-Engineer-Tasks/assets/94924061/4e0ac3a2-bea6-4060-a5d1-0e4872e1841f)


## solution
1. ssh into the App server 1
```
ssh username@ip_addr
```

2. create a user and specify expiry date with -e flag
```
useradd -e 2021-01-28 mark
```

3. To confirm user is created with the above requirements
```
sudo chage -l mark
```


