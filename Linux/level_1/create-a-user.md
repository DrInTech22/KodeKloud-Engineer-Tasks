# create a user

## Task
a. Create a user named ravi on the App server 3 in Stratos Datacenter.

b. Set its UID to 1873 and home directory to /var/www/ravi.

## solution
1. Create user using the 'usermod' command.
```adduser ravi -m -d /var/www/ravi```

-   -m & -d flag to create a custom home directory.

2. Set the newly created user UID to 1873
```usermod -u 1944 ravi```

-   -u flag will set the defined uid to specified user.
