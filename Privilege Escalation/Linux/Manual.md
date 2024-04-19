List sudo privileges of current user:
```bash
sudo -l
```

Print history:
```bash
history
```

Search for SUID executables:
```bash
find / -perm -u=s -type f 2>/dev/null
```
