## Show Gateway Address

```sh
ip gateway
```

## Show ARP Table

```sh
ip neigh
```

## Show All Open Ports

```sh
sudo netstat -tunlp
```

- `-t` - Show TCP ports
- `-u` - Show UDP ports
- `-n` - Show numerical addresses instead of resolving hosts
- `-l` - Show only listening ports
- `-p` - Show the PID and name of the listener’s process (shown only if permitted)

## RDP to Host

```sh
xfreerdp /u:$username /p:$password /v:$ip /dynamic-resolution
```
