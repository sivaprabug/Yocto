# Copying Images to SD Card

We have formatted our card, according to the requirements. 

 Now, we are ready to populate images to it. 

The partitions are usually auto mounted under /media/$USER

If not, we can use the mount command to mount the partition to our desired location:

$ sudo mount /dev/sdb1 /media/$USER/BOOT
$ sudo mount /dev/sdb2 /media/$USER/ROOT

Now, follow these steps to copy images to the card:

1. Copy the u-boot MLO and u-boot bootloader images into the FAT32 partition:

$ sudo cp MLO /media/$USER/BOOT
$ sudo cp u-boot.img /media/$USER/BOOT

2. Copy the kernel image into the boot partition:


$ sudo cp zImage /media/$USER/BOOT 


3. Copy the .dtb file, am335x-boneblack.dtb, into the boot partition. This step is required only in the case of core-image-minimal. It is not required in our case, as we created core-image-sato, which already has this file placed at the desired location in rootfs:

$ sudo cp am335x-boneblack.dtb /media/$USER/BOOT 

4. As a root user, uncompress core-image-sato-beaglebone.tar.bz2 to the ext4 partition:

$ sudo tar -xf core-image-minimal-beaglebone-yocto.tar.bz2 -C /media/$USER/ROOT/
5. Unmount both partitions:

$ sudo umount /dev/mmcblk0p1
$ sudo umount /dev/mmcblk0p2

Remove the card from the host machine, and insert it into the SD card slot on BeagleBone Black.

