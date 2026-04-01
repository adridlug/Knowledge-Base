### dd

Skip 0x40000 blocks in $INPUT file and write content to $OUTPUT file. bs specifies the size of one block. Default is 512.
```
dd bs=1 if=$INPUTFILE skip=$((0x400000)) of=$OUTPUTFILE
```
Write some bytes into a file <br>
```
printf "%b" '\x66\x6f\x6f' > $OUTPUTFILE
```

