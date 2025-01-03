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
# Firewall and IDS/IPS Evasion

https://nmap.org/book/man-bypass-firewalls-ids.html

## TCP ACK scan (`-sA`)

Packets with the `ACK` flag are often passed by the firewall because the firewall cannot determine whether the connection was first established from the external network or the internal network.

## Detect IDS/IPS

One method to determine whether a IPS system is present in the target network is to scan from a single host (virtual private servers `VPS`). If at any time this host is blocked and has no access to the target network, we know that the administrator has taken some security measures. Accordingly, we can continue our penetration test with another `VPS`.

## DNS Proxying

Packets with a specific source port (e.g. TCP port 53 for DNS) may be whitelisted by the firewall.
```
sudo <nmap cmd> --source-port 53
```

---
# Some additional options

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