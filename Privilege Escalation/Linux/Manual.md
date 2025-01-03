GTFOBins:
https://gtfobins.github.io/

# Checklists

https://swisskyrepo.github.io/InternalAllTheThings/redteam/escalation/linux-privilege-escalation/

https://book.hacktricks.xyz/linux-hardening/linux-privilege-escalation-checklist

# Commands

Show Linux version:
```bash
uname -a
```

List sudo privileges of current user:
```bash
sudo -l
```

Print groups of current user:
```bash
groups
```

Print history:
```bash
history
```

Search hidden files in home directory:
```bash
ls -la ~
```

List users:
```bash
cat /etc/passwd
```

Search for SUID executables:
```bash
find / -perm -u=s -type f 2>/dev/null
```

List running processes:
```bash
ps -aux
```

List cron jobs:
```bash
cat /etc/crontab
ls -l /etc/cron*
ls -l /var/spool/cron/crontabs
```

List open ports:
```bash
netstat -tulpn
```

Print environment variables:
```bash
printenv
```

Search for strings in files:
```bash
grep --color=auto -rnw '/' -iIe "PASSW\|PASSWD\|PASSWORD\|PWD\|PASS\|PW" --color=always --exclude-dir={usr,lib,boot,bin,cache} 2>/dev/null
```

Show ARP table:
```bash
arp -a
ip neighbour
ip neigh
```

Show routing information:
```bash
ip route
route
```

Snoop on processes:
https://github.com/DominicBreuker/pspy
```bash
./pspy64
```

If you want to switch user and encounter this error:
```bash
su oracle
su: must be run from a terminal
```
Run this command and try again:
```bash
/usr/bin/script -qc /bin/bash /dev/null
su oracle
```
