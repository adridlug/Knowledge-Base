## Create Redirect Rule

```sh
iptables -t nat -A PREROUTING -i eth0 -p tcp --dport 25 -j REDIRECT --to-port 2525
```
_Redirect port 25 to 2525._

## List All Rules with Line Numbers

```sh
sudo iptables -t nat -L -n -v --line-numbers
```

## Delete Rule by Chain and Line

```sh
sudo iptables -D PREROUTING 1
```
_Deletes by chain PREROUTING and line number 1._

## Save Rules to File

```sh
sudo iptables-save > rule.v4
```

## Restore Rules from File

```sh
sudo iptables-restore -n rule.v4
```




