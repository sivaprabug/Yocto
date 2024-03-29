# Creating partitions and formatting the SD card

1. Unmount any mounted partition, using the umount command:

$  umount /dev/sdb1

2. Launch the fdisk utitility and delete the previous partition(s); in our case, it is just one:

$  sudo fdisk /dev/sdb
Command (m for help): d
Selected partition 1

3. Create new partition called BOOT of 32 MB and type primary:

Command (m for help): n
Partition type:
   p   primary (0 primary, 0 extended, 4 free)
   e   extended
Select (default p): 
Using default response p
Partition number (1-4, default 1): 
Using default value 1
First sector (2048-7774207, default 2048): 
Using default value 2048
Last sector, +sectors or +size{K,M,G} (2048-7774207, default 7774207): +32M

4. Create a second partition to hold rootfs. We will give all the remaining space to this partition:

Command (m for help): n
Partition type:
   p   primary (1 primary, 0 extended, 3 free)
   e   extended
Select (default p): 
Using default response p
Partition number (1-4, default 2): 
Using default value 2
First sector (67584-7774207, default 67584): 
Using default value 67584
Last sector, +sectors or +size{K,M,G} (67584-7774207, default 7774207): 
Using default value 7774207

5. Make the first partition bootable by setting the boot flag:

Command (m for help): a
Partition number (1-4): 1

6. Set the first partition as WIN95 FAT32 (LBA):

Command (m for help): t Selected partition 1 Hex code (type L to list codes): c

7. We are done with the filesystem modification. So, let's write it by issuing the w command:

Command (m for help): w
The partition table has been altered!
Calling ioctl() to re-read partition table.
Syncing disks.

Tip
Do not forget to set the first partition as WIN95 FAT32 (LBA); otherwise, BeagleBone won't be able to boot from it. In this case, you might end up wasting time figuring out what's going wrong.

8. Format the first partition as FAT, using the following command. We will set the label as BOOT so that we know what directory it will be mounted to by udisks:

$  sudo mkfs.vfat -n "BOOT" /dev/sdb1

9. Format the second partition as an ext4 filesystem, using the following command. The label for this is set to ROOT, as it will contain the extracted image of rootfs.

$  sudo mkfs.ext4 -L "ROOT" /dev/sdb2
