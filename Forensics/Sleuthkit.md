### mmls
`mmls $IMAGE` retrievs information about partitioning table

### fstat
`fsstat $IMAGE` retrieves information about the filesystem

### blkls
blkls opens the named image(s) and copies file system data units (blocks).<br>
`blkls -f lsit` lists all supported filetytes

### fls
`fls -p $IMAGE` list all directories and files in an image

### icat
`icat $IMAGE $ID` extracts the file from an image. $ID is taken from the output of `fls`

### istat
`istat $IMAGE $ID` shows inode informations for the given $ID
