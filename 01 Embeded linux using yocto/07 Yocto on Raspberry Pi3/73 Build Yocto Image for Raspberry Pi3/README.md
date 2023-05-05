# Build Yocto Image for Raspberry Pi3

## Images

rpi-hwup-image.bb: This is an image based on core-image-minimal

rpi-basic-image.bb: This is an image based on rpi-hwup-image.bb, with some added features (a splash screen)

rpi-test-image.bb: This is an image based on rpi-basic-image.bb, which includes some packages present in meta-raspberrypi

## Enabling UART

RaspberryPi 3 does not have the UART enabled by default because this needs a fixed core frequency and enable_uart wil set it to the minimum

To enable it, set the following in local.conf

ENABLE_UART = "1"

```shell
bitbake rpi-hwup-image
```
