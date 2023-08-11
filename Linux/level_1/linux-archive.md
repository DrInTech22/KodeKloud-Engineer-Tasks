
# Linux Archives
On Nautilus storage server in Stratos DC, there is a storage location named /data, which is used by different developers to keep their data (non confidential data). One of the developers named siva has raised a ticket and asked for a copy of their data present in /data/siva directory on storage server. /home is a FTP location on storage server itself where developers can download their data. Below are the instructions shared by the system admin team to accomplish this task.



## Task
a. Make a siva.tar.gz compressed archive of /data/siva directory and move the archive to /home directory on Storage Server.

![Screenshot (32)](https://github.com/DrInTech22/KodeKloud-Engineer-Tasks/assets/94924061/b9776037-e03e-419a-9962-4bc795bda522)


## solution
1. ssh into the Storage server
```
ssh username@ip_addr
```
  switch to root user
```
sudo su
```
2. Compress files using tar command

```
tar -cvzf siva.tar.gz /data/siva
```
Note:
- -c : creates a tar archive
- -v : stands for verbose. It returns info on file compressed.
- -z : compresses file or directory
- -f : receives the file name or directory  




3. move archive to /home

```
mv siva.tar.gz /home
```





