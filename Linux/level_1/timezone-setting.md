
# Linux TimeZones Setting

During the daily standup, it was pointed out that the timezone across Nautilus Application Servers in Stratos Datacenter doesn't match with that of the local datacenter's timezone, which is Pacific/Enderbury.

## Task
Correct the mismatch.

## solution
1. login to app server 1 
```
ssh user@ip_addr
```

2. view the current timezone using timedatectl command
```
timedatectl
```

3. change the timezone using the set-timezone sub-command
```
timedatectl set-timezone Pacific/Enderbury
```
4. repeat this on other app Servers 

