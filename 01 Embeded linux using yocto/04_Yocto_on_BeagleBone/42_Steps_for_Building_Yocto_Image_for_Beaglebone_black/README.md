# Steps for Building Yocto Image for Beaglebone black

BeagleBone is one of the reference boards of Yocto Project

```shell
source poky/oe-init-build-env build_bbb
```

Open build_bbb/local.conf file

        comment out the default selection, which is the qemux86_64
        uncomment the beaglebone selection

        MACHINE ?= "beaglebone-yocto"
        #MACHINE ??= "qemux86_64"

Trigger build

```shell
bitbake core-image-minimal

```

After the build is complete, you will have your images ready at tmp/deploy/images/beaglebone-yocto/

This folder contains
        first-level bootloader MLO,
        second-level bootloader u-boot,
        kernel image,
        device tree blobs,
        a root filesystem archive, and
        a modules archive.