# TCP

Scan for open TCP ports:
```bash
nmap -v -Pn -p- -oA tcp_all <ip>
```

Enumerate services:
```bash
nmap -v -Pn -p <ports> -sV -sC -oA tcp_services <ip>
```

# UDP

Scan for top UDP ports:
```bash
sudo nmap -v -Pn -sU -oA udp_default <ip>
```
