# HTTP

Python3 webserver:
```bash
python3 -m http.server 80 -d .
```

Python2 webserver:
```bash
python2 -m SimpleHTTPServer 80
```

# FTP

Allow anonymous login. Edit */etc/vsftpd.conf*:
```
anonymous_enable=YES
```

Start FTP server:
```bash
sudo systemctl start vsftpd
```

Connect to FTP server from Linux:
```bash
ftp <ip>
```

Connect to FTP server from Windows:
- Right-click in the explorer -> "Add a network location"
- "Choose a custom network location"
- Specify server address: `ftp://<ip>`

# Netcat

On sending system (attacker machine):
```bash
cat file.zip | nc <ip> <port>
```

On receiving system (target machine):
```bash
nc -vlnp -q 1 <port> > file.zip
```
