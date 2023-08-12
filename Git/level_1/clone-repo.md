
# Git clone repository
DevOps team created a new Git repository last week; however, as of now no team is using it. The Nautilus application development team recently asked for a copy of that repo on Storage server in Stratos DC. Please clone the repo as per details shared below:






## Task
a. The repo that needs to be cloned is /opt/official.git
b. Clone this git repository under /usr/src/kodekloudrepos directory. Please do not try to make any changes in the repo.


![Screenshot (35)](https://github.com/DrInTech22/KodeKloud-Engineer-Tasks/assets/94924061/f02ab549-7245-40c8-863c-9795c43a1c8f)

## solution
1. ssh into the Storage server
```
ssh username@ip_addr
```
  switch to root user
```
sudo su
```
2. switch directory to /usr/src/kodekloudrepos

```
cd /usr/src/kodekloudrepos
```

3. clone git repo 

```
git clone /opt/official.git
```





