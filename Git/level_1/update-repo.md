
# Git Repository Update

The Nautilus development team started with new project development. They have created different Git repositories to manage respective project's source code. One of the repositories /opt/news.git was created recently. The team has given us a sample index.html file that is currently present on jump host under /tmp directory. The repository has been cloned at /usr/src/kodekloudrepos on storage server in Stratos DC.






## Task
a. Copy sample index.html file from jump host to storage server under cloned repository at /usr/src/kodekloudrepos/news, further add/commit the file and push to the master branch.

## solution
1. copy file from jump host to /tmp on storage server
```
scp /tmp/index.html natasha@ststor01:/tm
```

2. ssh into storage server and copy file to cloned repo
```
ssh natasha@ststor01
```
```
cp /tmp/index.html /usr/src/kodekloudrepos/news
```

3. stage the file, commit and push to master branch
```
cd  /usr/src/kodekloudrepos/news
```
```
git add index.html
```
```
git commit -m "add index.html"
```
```
git push origin master
```

![Screenshot (37)](https://github.com/DrInTech22/KodeKloud-Engineer-Tasks/assets/94924061/f93ba8bc-a9ae-44f2-872e-aed3754ec4b5)


