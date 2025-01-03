# TCP

Scan for open TCP ports:
```bash
nmap -v -Pn -p- -T4 -oA tcp_all <ip>
```

Enumerate services:
```bash
nmap -v -Pn -p <ports> -T4 -sV -sC -oA tcp_services <ip>
```

# UDP

Scan for top UDP ports:
```bash
sudo nmap -v -Pn -sU -T4 -oA udp_default <ip>
```

When version scanning is enabled with `-sV` the scan takes long but might reveal open ports which will otherwise be hidden, i.e. marked `open|filtered` and thus ignored.

Scan for top UDP ports with version scanning:
```bash
sudo nmap -v -Pn -sU -sV -T4 -oA udp_default <ip>
```

---
# Additional options

| Argument             | Description                                                              |
| -------------------- | ------------------------------------------------------------------------ |
| `--packet-trace`     | Shows all packets sent and received.                                     |
| `--reason`           | Displays the reason for specific result.                                 |
| `-PE`                | Performs the ping scan by using 'ICMP Echo requests' against the target. |
| `--disable-arp-ping` | disable ARP pings. (If we want to use `-PE` we need to use this option)  |
# Scripts

Nmap scripts are located at `/usr/share/nmap/scripts/`

List all default scripts (executed with the `-sC` option): 
```
grep '"default"' -R -l /usr/share/nmap/scripts/
```

Nmap has a script category `vuln` which can be used to identify vulnerabilities in the services:
```
<nmap cmd> --script vuln
```

# Port states

Explanation of port states: https://nmap.org/book/man-port-scanning-basics.html 