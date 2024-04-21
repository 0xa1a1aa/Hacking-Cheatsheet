Local port forwarding (localhost:port is forwarded to remote host:port):
```bash
ssh -N -L <lport>:<rhost>:<rport> <user>@<ssh-server-host>
```

Remote port forwarding (remote host:port is forwarded to localhost:port):
```bash
ssh -N -R <rport>:<lhost>:<lport> <user>@<ssh-server-host>
```