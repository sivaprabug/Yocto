# Use gparted to create or format or partitions

#First partition
type: FAT32
size: around 30MB
label: BOOT
flags: boot
 
#Second partition
type: ext4
size: around 200MB, or rest of SD-card
label: ROOT

