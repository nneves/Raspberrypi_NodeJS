Raspberrypi NodeJS
------------------

Instructions to compile Node.js on a Raspberry Pi (Embedded ARM board running Linux Debian)


Compile Node.js v0.8.10 on a RaspberryPi with Linux Debian armhf (hardware floating point) wheezy (raspbian)
===========================================================================================================
Note: no more V8 code patching required!

distro: 2012-09-18-wheezy-raspbian.zip

Install the necessary dependecies:
```bash
sudo apt-get install git-core build-essential libssl-dev
```

Get Node.js source:
```bash
git clone -b v0.8.10 git://github.com/joyent/node.git
cd node
```

Configure and make (disable snapshot):
```bash
./configure --shared-openssl --without-snapshot

time make CFLAGS+=-O2 CXXFLAGS+=-O2 install
```

Install
```bash
sudo make install
```

Old instructions (no longer required - available for historic purpose only)
----------------

Compile Node.js v0.8.x on a RaspberryPi with Linux Debian armhf (hardware floating point) wheezy (raspbian)
===========================================================================================================
https://github.com/nneves/Raspberrypi_NodeJS/blob/master/Compile_RaspberryPi_NodeV0.8.x.md#compile-nodejs-v08x-on-a-raspberrypi-with-linux-debian-armhf-hardware-floating-point-wheezy-raspbian

Compile Node.js v0.8.x on a RaspberryPi with Linux Debian armel wheezy
======================================================================
https://github.com/nneves/Raspberrypi_NodeJS/blob/master/Compile_RaspberryPi_NodeV0.8.x.md#compile-nodejs-v08x-on-a-raspberrypi-with-linux-debian-armel-wheezy


Compile Node.js v0.6.20 on a RaspberryPi with Linux Debian armel squeeze/wheezy
======================================================================
https://github.com/nneves/Raspberrypi_NodeJS/blob/master/Compile_RaspberryPi_NodeV0.6.20.md