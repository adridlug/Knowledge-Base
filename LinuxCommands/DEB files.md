## Execute Script After Debian Package Installation

1. Create a temporary directory:
	```sh
	mkdir temp
	```
2. Extract the deb file:
	```sh
	dpkg-deb -x $DEBFILE temp/
	```
3. Copy files as needed:
	```sh
	cp /temp
	```
4. Extract control information:
	```sh
	dpkg-deb -e ../$DEBFILE
	```
5. Add your command to the post-install script:
	```sh
	echo $COMMAND > DEBIAN/postinst
	```
6. Make the post-install script executable:
	```sh
	chmod +x DEBIAN/postinst
	```
7. Recreate the deb file:
	```sh
	dpkg-deb -b . $DEBFILE
	```

## Install Package

```sh
dpkg-deb -i $DEBFILE
```
