## Start Service

```sh
sudo service $servicename start
```
or
```sh
sudo systemctl start $servicename
```

## Restart Service

```sh
sudo service $servicename restart
```
or
```sh
sudo systemctl restart $servicename
```

## Stop Service

```sh
sudo service $servicename stop
```
or
```sh
sudo systemctl stop $servicename
```

## List Active and Inactive Services

```sh
systemctl list-units --type=service
```

## List Running Services

```sh
systemctl list-units --type=service --state=running
```

