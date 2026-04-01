# VirtualBox Installation

1. Update package lists:
	```sh
	sudo apt update
	```
2. Upgrade all packages:
	```sh
	sudo apt full-upgrade -y
	```
3. Reboot if required:
	```sh
	[ -f /var/run/reboot-required ] && sudo reboot -f
	```
4. Import VirtualBox's repo keys:
	```sh
	curl -fsSL https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/oracle_vbox_2016.gpg
	curl -fsSL https://www.virtualbox.org/download/oracle_vbox.asc | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/oracle_vbox.gpg
	```
5. Add VirtualBox's repo:
	```sh
	echo "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian bullseye contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list
	```
6. Rebuild cache after network repo has been altered:
	```sh
	sudo apt update
	```
7. Install DKMS (to keep kernel modules up-to-date):
	```sh
	sudo apt install -y dkms
	```
8. Install VirtualBox and extension pack:
	```sh
	sudo apt install -y virtualbox virtualbox-ext-pack
	```
9. Start VirtualBox:
	```sh
	virtualbox
	```
