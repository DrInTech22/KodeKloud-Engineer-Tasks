
# Linux User Files
After doing some security audits of servers, xFusionCorp Industries security team has implemented some new security policies. One of them is to disable direct root login through SSH.






## Task
a. Disable direct SSH root login on all app servers in Stratos Datacenter.

![Screenshot (26)](https://github.com/DrInTech22/KodeKloud-Engineer-Tasks/assets/94924061/91c5be4e-c96d-44e9-957f-670df7c2e53a)

## solution
1. ssh into the App server 1
```
ssh username@ip_addr
```
2. open sshd config file with vi editor
```
sudo vi  /etc/ssh/sshd_config
```
3. change PermitRootLogin from yes to no
```
PermitRootLogin  no
```
4. Restart to sshd service for the changes to take effect.
```
# sudo systemctl restart sshd
```




