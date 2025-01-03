# HTTP

Python3 web server:
```bash
python3 -m http.server 80 -d .
```

Python2 web server:
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

# Base64

Base64 encode a file to transfer locally, copy-paste the base64 string to the remote host and decode it into a file.

Encode file to transfer on local machine:
```
cat file | base64
```

Decode file on remote machine:
```
echo <base64-string> | base64 -d > file
```