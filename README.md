Raspberrypi NodeJS (Embedded ARM board running Linux Debian)
==================

Pre-Compiled binaries of node.js for Raspberry Pi
------------------

https://gist.github.com/3245130


Instructions to compile Node.js on a Raspberry Pi
------------------

Compile Node.js v0.8.10 on a RaspberryPi with Linux Debian armhf (hardware floating point) wheezy (raspbian)
===========================================================================================================
Note: no more V8 code patching required!
Source: https://gist.github.com/3245130#gistcomment-399244

distro: 2012-09-18-wheezy-raspbian.zip

Install the necessary dependecies:
```bash
sudo apt-get install build-essential libssl-dev
```

Get Node.js source:
```bash

export NODE_VER=0.8.10

curl http://nodejs.org/dist/v$NODE_VER/node-v$NODE_VER.tar.gz | tar xz

cd node-v$NODE_VER
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