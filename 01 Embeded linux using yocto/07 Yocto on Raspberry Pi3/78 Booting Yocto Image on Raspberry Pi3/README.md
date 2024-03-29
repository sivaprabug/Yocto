# Raspberry Pi Zero W and Yocto

- 1GHz, Single-core CPU

- 512MB RAM

- Mini HDMI and USB On-The-Go ports

- Micro USB power

- HAT-compatible 40-pin header

- Composite video and reset headers

- CSI camera connector

- 802.11n wireless LAN

- Bluetooth 4.0

## Steps for generating Yocto Image

- Everything is same except MACHINE = 'raspberrypi0-wifi'

Find the kernel

```shell
uname -a
```

Find how many processes?

```shell
nproc
```

Verify the memmory

```shell
free -m
```

Verify the command line

```shell
cat /proc/cmdline
```

Connect via ssh

```shell
ssh pi@192.168.0.100
```

Verify ssh module enabled or not

```shell
ps -ef | grep dropbear
ps | grep dropbear
```
