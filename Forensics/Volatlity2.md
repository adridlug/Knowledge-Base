# Volatility 2

## Install volatiltiy2
execute following script<br>
```
#!/bin/bash

sudo apt install python2

#install pip2
wget https://bootstrap.pypa.io/pip/2.7/get-pip.py
sudo python2 get-pip.py

# Prerequisites
sudo apt-get install build-essential autoconf dwarfdump git subversion pcregrep libpcre++-dev python-dev -y

# install distorm3
pip2 install distorm3

# install yara
wget https://github.com/VirusTotal/yara/archive/refs/tags/v4.0.1.tar.gz
tar -zxf v4.0.1.tar.gz
cd yara-4.0.1
sudo apt-get install automake libtool make gcc pkg-config
./bootstrap.sh
./configure
make
sudo make install
make check
cd ..

# install PyCrypto
pip2 install PyCrypto

#install vol2
git clone https://github.com/volatilityfoundation/volatility.git
cd volatility

```
