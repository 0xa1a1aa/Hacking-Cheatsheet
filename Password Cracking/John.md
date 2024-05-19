Use `hash-identifier` to identify the hash format.

Crack the hash stored in *passwd.txt*:
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt --format=md5crypt passwd.txt
```

# ZIP files

Convert zip:
```bash
zip2john file.zip > hash.txt
```

Crack the hash:
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```

# SSH Private Key

Convert private key:
```bash
ssh2john id_rsa > id_rsa.hash
```

Crack the hash:
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt id_rsa.hash
```