# 3rd Stage Bootloader - U-Boot

U-BOOT allows for powerful command-based control over the kernel boot environment via a serial terminal

The user has control over a number of parameters such as boot arguments and the kernel boot command

In addition, U-boot environment variables can be configured. 

These environment variables are stored in the uEnv.txt file on your storage medium.

The built-in environment in u-boot loads a default am335x-boneblack.dts to pass to the kernel at boot.

In uEnv.txt you can explicitly specify a different DTS as well as the command line arguments to pass to the kernel

u-boot is also capable of obtaining network information via DHCP and loading it into environmental variables.

Finaly U-boot loads the kernel and a DTS into memory and boots the kernel with some command line arguments

The kernel initializes and mounts the root filesystem.

By default, the root filesystem is contained in the second partition (mmcblk0p2) of the microSD card, formatted for an ext3 file system.
