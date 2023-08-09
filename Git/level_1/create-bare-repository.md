
# Git Install and Create Bare Repository
The Nautilus development team shared requirements with the DevOps team regarding new application development.—specifically, they want to set up a Git repository for that project. Create a Git repository on Storage server in Stratos DC as per details given below: 






## Task
a. Install git package using yum on Storage server.
b. After that create a bare repository /opt/demo.git (make sure to use exact name).

## solution
1. ssh into the Storage server
```
ssh username@ip_addr
```
  switch to root user
```
sudo su
```
2. Install git using yum 
```
yum install git 
```
3. create git bare repository
note: git bare repository is a repository that has no working directory(can't commit changes on it) and it's basically used for setting up git server to share code between developers.
```
mkdir /opt/demo.git
cd /opt/demo.git
git init --bare
```





