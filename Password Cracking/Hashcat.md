Crack MD5 hash:
```bash
hashcat -m 0 hashes.txt /usr/share/wordlists/rockyou.txt
```

NTLM:
```bash
hashcat --help | grep NTLM
```
Crack NTLMv2 hash:
```bash
hashcat -m 5600 ntlmv2_hash.txt /usr/share/wordlists/rockyou.txt
```