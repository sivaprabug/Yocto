# Flashing images on SD Card

- Images are present in tmp/deploy/images/raspberrypi3

```shell
lsblk
```

```shell
sudo dd if=rpi-hwup-image-raspberrypi3.rpi-sdimg of=/dev/sdb bs=4096 && sync
```
