# Linux Remote Copy


One of the Nautilus developers has copied confidential data on the jump host in Stratos DC. That data must be copied to one of the app servers. Because developers do not have access to app servers, they asked the system admins team to accomplish the task for them.

## Task
Copy /tmp/nautilus.txt.gpg file from jump server to App Server 2 at location /home/data.

## solution
Use SCP command to copy the data from jump host to the specified app server

```
scp /tmp/nautilus.txt.gpg steve@stapp02:/home/data
```