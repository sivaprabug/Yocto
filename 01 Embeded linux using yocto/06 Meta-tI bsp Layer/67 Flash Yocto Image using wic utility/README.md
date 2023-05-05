# Flashing the image on the SD Card using wic

wic images are SD Card images and can be directly written into sd-card

core-image-minimal-beaglebone.wic.xz is compressed wic image.

It can be uncompressed using the unxz utility

```shell
unxz core-image-minimal-beaglebone.wic.xz
```

```shell
ls -lh core-image-minimal-beaglebone.wic
```

Flash it to the sd card

```shell
lsblk
```

```shell
sudo dd if=core-image-minimal-beaglebone.wic of=/dev/sdb bs=4096 status=progress && sync
```
