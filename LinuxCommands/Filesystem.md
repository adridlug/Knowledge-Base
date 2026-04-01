## show directory tree
```
tree -L 1 auxiliary/
```
## mount
```
mount -o rw, vers=3 $ip:$remotepath $localpath
```
**-o rw,vers=3** Options for the mount command</br>
**rw** Mount the filesystem with read and write permissions</br>
**vers=3** Specify the NFS version to use (in this case, version 3)</br>
