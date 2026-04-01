## find a file 
`find -name {TARGET}`
## print working dir
`pwd`
## List directories
List content of directory folder
`ls folder`
View hidden foldes
`ls -a `
List permissions
`ls -lh`


## Appends contet to a file (no overwrite)
`echo hello >> file.txt`

## Create file
`touch file.txt`

## Get file type
`file file.txt`

## Copy file remotly
### copy from local to remote
`scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt` 
### copy from remote to local
`scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt`

# Web server
Starting a web server `python3 -m http.server`

# Processes
Show all running processes by users session
`ps`<br>
Show all running processes by other users + different sessions
`ps aus`<br>
Real time stats of processes 
`top` <br>
Kill process `kill <pid>` SIGTERM=with clean up, SIGKILL=without clean up, SiGSTOP = suspend,stop<br>
Start apache server on startup `systemctl start apache2` <br>
run command in the background `echo "Hallo" &`<br>
bring process from backtrou to foreground `fg`<br>
# cron
Show all cronjobs `crontab -e`<br>
Useful links
https://crontab-generator.org/
https://crontab.guru/
# apt
Add repository`add-apt-repository`<br>
Download the GPG key and use apt-key to trust it<br>
`wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`<br>
Remove package <br>
`add-apt-repository --remove ppa:PPA_Name/ppa`

# OpenVPN
Create connection <br>
`sudo openvpn --config $CONFIGFILE --deamon` use deamon in order to not run two processes <br>
fix mtu size when pulling data during TryHackMe chalanges hangs <br>
`sudo ip link set dev <INTERFACE> mtu 1200`<br>
check mtu on tun0 <br>
`sudo ip link show dev tun0` <br>
if mtu is not 1200 then update
`sudo ip link set dev tun0 mtu 1200`
# git
### set user name and email
`git config --global user.name "$USER"`<br>
`git config --global user.email "$MAIL"`

### install kernel headers
`sudo apt-get install linux-headers-$(uname -r)`

### install bundle
`chmod +x $BUNDLEFILE`<br>
`./$BUNDLEFILE`

### fix broken dependencies
`sudo apt --fix-broken install`

### reverse hex string into binary data
```
echo $HEXVALUE > tmp.txt
xxd -r -p tmp.txt > $OUTPUT
```
### list all programs which can be run with sudo
```
sudo -l
```
### list all shared libs of a program
```
ldd $pathtoprogram
```
### locate a file
```
locate $file
```
### monitor system calls and signals of a program
```
strace $program
```
### check bash version
```
/bin/bash --version
```
### check command history
```
cat ~/.*history | less
```
