# TCP

Scan for open TCP ports:
```bash
nmap -Pn -p- -oN tcp_all.nmap <ip>
```

Enumerate services:
```bash
nmap -Pn -p <ports> -sV -sC -oN tcp_services.nmap <ip>
```

# UDP

Scan for top UDP ports:
```bash
sudo nmap -Pn -sU -oN udp_default.nmap <ip>
```
