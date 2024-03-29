# Steps to generate an Yocto Image for Raspberry Pi3

Poky has no support for Broadcom BCM SoC.

Step1: Download the BSP Layer for Raspberry Pi3

```shell
git clone git://git.yoctoproject.org/meta-raspberrypi
```

Step2: Download meta-openembedded branch as meta-raspberrypi layer depends upon it

```shell
git clone git://git.openembedded.org/meta-openembedded
```

Step3: Once you complete cloning, there should be three folders: poky, meta-openembedded, meta-raspberrypi

```shell
ls source
```

Step4: Run the environment script to setup the Yocto Environment and create build directory

```shell
source poky/oe-init-build-env build_pi
```

Step5: Add meta-openembedded layers ( meta-oe, meta-multimedia, meta-networking, meta-python) and meta-raspberrypi layer to bblayers.conf

Step6: Set the MACHINE in local.conf to "raspberrypi3".

```shell
echo 'MACHINE = "raspberrypi3"' >> conf/local.conf
```

Step7: Final step is to build the image. To find out the available images:

```shell
ls ../meta-raspberrypi/recipes-*/images/
```
