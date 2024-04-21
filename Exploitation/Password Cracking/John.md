Crack the hash stored in *passwd.txt*:
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt --format=md5crypt passwd.txt
```
Use `hash-identifier` to identify the hash format