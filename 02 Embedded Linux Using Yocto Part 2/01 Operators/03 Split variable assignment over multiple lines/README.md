# Line Joining

BitBake joins any line ending in a backslash character ("\") with the following line before parsing statements

The most common use for the "\" character is to split variable assignments over multiple lines

BBLAYERS ?= " \
  /home/linuxtrainer/Yocto_Training/source/poky/meta \
  /home/linuxtrainer/Yocto_Training/source/poky/meta-poky \
  /home/linuxtrainer/Yocto_Training/source/poky/meta-yocto-bsp \
  "
  
```shell
bitbake -e | grep ^BBLAYERS
```
