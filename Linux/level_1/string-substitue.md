
# Linux String Substitute

The backup server in the Stratos DC contains several template XML files used by the Nautilus application. However, these template XML files must be populated with valid data before they can be used. One of the daily tasks of a system admin working in the xFusionCorp industries is to apply string and file manipulation commands!

## Task
Replace all occurances of the string Text to Cloud on the XML file /root/nautilus.xml located in the backup server.

## solution
1. login to backup server 
```
ssh user@ip_addr
```
```
sudo su
```

2. Use the sed command to change every occurence of 'Text' to 'Cloud'
```
cat nautilus.xml | grep Text 
```
```
sed -i 's/Text/Cloud/g' /root/nautilus.xml
```

3. validate all occurence of text has been Substituted 
```
cat nautilus.xml | grep Text 
```

```
cat nautilus.xml | grep Cloud
```
