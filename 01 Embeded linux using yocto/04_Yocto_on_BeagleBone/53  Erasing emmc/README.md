# Yocto booting on Beagle Bone Black


Now that we have everything set up, we are ready to boot.

We can just insert this card, and our board should boot from it. 

There might be only one issue if you have the eMMC (embedded MultiMediaCard) boot selected by default. 

You will have to disable it by booting up the board from the images you already have and renaming the MLO file from the eMMC partition

Alternatively, you can simply execute the following two commands on the u-boot prompt. 

 To stop at the u-boot prompt, simply press Enter after powering up the board before timeout:

# mmc dev 1
# mmc erase 0 512

The first command will select the eMMC card, and the second one will do the erasing so that BeagleBone doesn't try to boot from eMMC.

Insert our prepared SD card and power up BeagleBone. You should get an output similar to the following one on minicom:

Booting from mmc ...
## Booting kernel from Legacy Image at 82000000 ...
   Image Name:   Linux-3.14.0-yocto-standard
   Image Type:   ARM Linux Kernel Image (uncompressed)
   Data Size:    4985768 Bytes = 4.8 MiB
   Load Address: 80008000
   Entry Point:  80008000
   Verifying Checksum ... OK
## Flattened Device Tree blob at 88000000
   Booting using the fdt blob at 0x88000000
   Loading Kernel Image ... OK
   Loading Device Tree to 8fff5000, end 8ffff207 ... OK
Starting kernel …

Finally, we will land in our BeagleBone prompt:

Poky (Yocto Project Reference Distro) 1.6.1 beaglebone /dev/ttyO0
beaglebone login:

Enter root as user, and you are in as the root user:

root@beaglebone:~# 


